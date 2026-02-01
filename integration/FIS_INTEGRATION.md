# Integrating Quill with fis

## The Relationship

**fis:** Story-specific pipeline (knows characters, world, themes)
**Quill:** Generic writing pipeline (works with any prose)

**They complement, not replace, each other.**

---

## Integration Strategies

### Strategy 1: Parallel Tools

**Use fis for:** Story-aware generation and refinement
**Use Quill for:** Quick polish and non-story content

```
fis/
├── story/              # Story context
├── agents/             # Story-aware agents
│   ├── story_architect_agent.md
│   ├── first_draft_agent.md
│   ├── prose_refinement_agent.md
│   └── leguin_reviewer_agent.md
├── drafts/             # Generated scenes
└── inbox/              # Reviews and iterations

# When working on story:
Use fis pipeline (has story context)

# When working on other writing:
cd ../quill
Use Quill pipeline (generic)
```

**Advantages:**
- Keep fis focused on story
- Use Quill for journal entries, essays, blog posts
- No mixing of concerns

---

### Strategy 2: Replace fis Refinement with Quill

**If you want unified refinement:**

1. **Keep fis for generation** (story-aware)
2. **Use Quill for refinement** (better craft focus)

```
fis workflow:
Story Architect → First Draft Agent (uses story context)
    ↓
    → ../quill/agents/refinement/refinement_coordinator.md
    ↓
Refined scene
```

**How to do it:**

In fis `pipeline_coordinator_agent.md`, change refinement step:

```markdown
### Stage 3 - First Prose Refinement:
- Invoke Prose Refinement Agent v1.3 on first draft
```

TO:

```markdown
### Stage 3 - First Prose Refinement:
- Hand off to Quill Refinement Pipeline
- Read: ../quill/agents/refinement/refinement_coordinator.md
- Apply with: type=fiction (full craft application)
```

**Advantages:**
- Unified refinement philosophy (craft > compression)
- Single source of truth for Le Guin principles
- Updates to Quill benefit fis

**Disadvantages:**
- Quill refinement doesn't know story context
- Can't check character voice consistency
- No thematic awareness

---

### Strategy 3: Quill as Preprocessing

**Use Quill before fis pipeline:**

```
Raw journal thoughts about story
    ↓
Quill Expansion Pipeline (structure ideas)
    ↓
Beats generated
    ↓
fis First Draft Agent (story-aware prose generation)
    ↓
fis Refinement (story-aware polish)
```

**Use case:**
- Start with loose journal musings about plot
- Quill structures them into beats
- fis generates story-aware prose from those beats

---

### Strategy 4: Skill Approach (Recommended)

**Make Quill a skill, use alongside fis:**

```bash
# Working in fis project
cd ~/code_repos/fis

# Generate scene with fis (story-aware)
[Use fis pipeline coordinator for story generation]

# Quick polish with Quill (generic but fast)
/refine drafts/movement2_s1_draft.md --type=fiction

# Or review quality
/review drafts/movement2_s1_refined.md

# Or expand journal thoughts
/expand "Ren's realization that the Aneth's stability is a cage"
```

**Advantages:**
- Both tools available simultaneously
- Choose right tool for the task
- No code changes needed
- Flexible usage

---

## Comparison: fis vs Quill

| Feature | fis Pipeline | Quill Pipeline |
|---------|-------------|----------------|
| **Story context** | Yes (knows characters, world) | No (generic) |
| **Input** | Story beats from Architect | Any idea or prose |
| **Generation** | Story-aware prose | Generic prose |
| **Refinement** | Story-aware polish | Craft-focused polish |
| **Review** | Story context aware | Pure craft assessment |
| **Use case** | Your novel project | Any writing |
| **Voice consistency** | Checks character voice | General Le Guin principles |
| **Thematic coherence** | Aware of themes | No theme awareness |
| **Speed** | Full pipeline (slower) | Quick refinement (faster) |

---

## Recommended Approach

### For Your fis Novel:

**Use fis pipeline for:**
- Scene generation from story beats
- Story-aware refinement
- Character voice consistency
- Thematic coherence

**Use Quill (as skill) for:**
- Quick polish on already-good scenes
- Journal entries about story ideas
- Blog posts about writing process
- Essays on themes
- Anything not requiring story context

### Workflow:

```bash
# Story generation (fis)
cd ~/code_repos/fis
[Run fis pipeline coordinator]
→ Generates story-aware prose

# Quick refinement (Quill skill)
/refine --type=fiction
→ Fast craft-focused polish

# Quality check (Quill skill)
/review
→ Pure craft assessment
```

---

## Implementation Steps

### Step 1: Install Quill as Skill

Follow `SKILL_SETUP.md` to make Quill available everywhere.

### Step 2: Keep fis As-Is

Don't modify fis. It's optimized for your story.

### Step 3: Use Both

- **fis** when story context matters
- **Quill** when generic refinement is enough
- **Quill** for all non-story writing

### Step 4: Optional - Create fis-quill Bridge

If you want to route fis output to Quill:

Create `fis/bridge_to_quill.sh`:

```bash
#!/bin/bash
# Takes fis output, sends to Quill refinement

SCENE_FILE=$1
cd ../quill

# Invoke Quill refinement
# (Implementation depends on how you call agents)

cd ../fis
```

---

## Example: Full Workflow

### Scenario: Writing Movement II, Scene 1

```bash
cd ~/code_repos/fis

# 1. Generate beats (fis Story Architect)
[Story Architect creates beats with story context]

# 2. Generate prose (fis First Draft Agent)
[First Draft generates story-aware prose]
→ Output: drafts/m2_s1_draft.md (1,500 words)

# 3. First refinement (fis Prose Refinement)
[Story-aware refinement, knows characters]
→ Output: drafts/m2_s1_refined.md (1,200 words)

# 4. Quick additional polish (Quill skill)
/refine drafts/m2_s1_refined.md --type=fiction
→ Pure craft polish, no story context needed
→ Output: drafts/m2_s1_final.md (1,100 words)

# 5. Quality check (Quill skill)
/review drafts/m2_s1_final.md
→ Le Guin craft assessment
→ Output: Reviews + scores
```

**Result:**
- Story context from fis
- Craft excellence from Quill
- Best of both worlds

---

## When to Choose Which

### Use fis Pipeline When:
- Generating new scenes from story beats
- Character voice matters
- Thematic coherence critical
- World-building consistency needed
- Story-specific refinement required

### Use Quill Pipeline When:
- Quick refinement without story context
- Journal entries (not part of story)
- Essays, blog posts, non-fiction
- Generic craft polish
- Learning Le Guin principles
- Working on non-fis projects

### Use Both When:
- fis generates, Quill polishes
- fis for story, Quill for meta-writing about story
- fis for fiction, Quill for everything else

---

## Advantages of Skill Approach

✓ **No code changes to fis** - Keep it working as-is
✓ **Available everywhere** - Use in fis or any project
✓ **Quick invocation** - `/refine` from anywhere
✓ **Complementary** - fis for story, Quill for craft
✓ **Flexible** - Choose right tool for task

---

## Summary

**Best approach: Make Quill a skill, use alongside fis.**

- fis remains your story pipeline (context-aware)
- Quill becomes your craft assistant (context-free)
- Both available in any project
- No duplication or conflicts
- Flexibility to use either or both

**Next step:** Follow `SKILL_SETUP.md` to install Quill as a skill.
