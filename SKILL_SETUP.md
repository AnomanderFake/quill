# Using Quill as a Claude Code Skill

## Setup

### 1. Create Skill Definition

In your `~/.claude/skills/` directory, create `quill.md`:

```markdown
# Quill Writing Assistant

## Skill Definition

**Name:** quill
**Aliases:** refine, expand, review
**Description:** Le Guin-inspired writing assistance - refine prose, generate from ideas, or review quality

---

## Commands

### /refine [--type=TYPE]
Refine prose using Le Guin principles.

**Usage:**
- `/refine` - Refine selected text or ask for input
- `/refine --type=journal` - Use moderate compression (10-20%)
- `/refine --type=fiction` - Use full craft application (20-40%)
- `/refine --type=essay` - Balanced approach (15-30%)

**Process:**
1. Detect or ask for text
2. Route to Quill Refinement Pipeline
3. Apply appropriate compression based on type
4. Return refined text + quality scores

---

### /expand [--mode=MODE]
Generate prose from ideas.

**Usage:**
- `/expand` - Generate from idea
- `/expand --mode=beats` - Show beats first, then generate
- `/expand --mode=full` - Generate + refine in one pass

**Process:**
1. Get idea from user
2. Route to Quill Expansion Pipeline
3. Generate beats → prose
4. Optionally refine

---

### /review
Quality check against Le Guin standard.

**Usage:**
- `/review` - Review selected text or ask for input

**Process:**
1. Get text
2. Route to Quality Reviewer only
3. Return scores + specific feedback
4. No changes made

---

## Implementation

**Location:** `/Users/ramachandrakoganti/Desktop/code_repos/quill/`

**Agents:**
- Refinement: `agents/refinement/refinement_coordinator.md`
- Expansion: `agents/expansion/expansion_coordinator.md`
- Master: `agents/master_orchestrator.md`

**How to invoke:**
When skill is called, route to appropriate Quill agent based on command.
```

---

### 2. Create Skill Handler (Optional Helper Script)

For convenience, create `quill-skill.sh` in quill directory:

```bash
#!/bin/bash

QUILL_DIR="/Users/ramachandrakoganti/Desktop/code_repos/quill"

case "$1" in
  refine)
    echo "Routing to Refinement Pipeline..."
    echo "Type: ${2:-auto-detect}"
    echo "Reading: $QUILL_DIR/agents/refinement/refinement_coordinator.md"
    ;;
  expand)
    echo "Routing to Expansion Pipeline..."
    echo "Mode: ${2:-full}"
    echo "Reading: $QUILL_DIR/agents/expansion/expansion_coordinator.md"
    ;;
  review)
    echo "Routing to Quality Reviewer..."
    echo "Reading: $QUILL_DIR/agents/refinement/quality_reviewer.md"
    ;;
  *)
    echo "Routing to Master Orchestrator..."
    echo "Reading: $QUILL_DIR/agents/master_orchestrator.md"
    ;;
esac
```

---

## Usage Examples

### In Any Project:

```bash
# Working on fis novel
cd ~/code_repos/fis
# Quick refinement of a scene
/refine --type=fiction

# Working on journal
cd ~/Documents/journal
# Light touch refinement
/refine --type=journal

# Plotting new scene
cd ~/code_repos/fis
# Generate from concept
/expand "scene where Ren realizes the valley isn't home"
```

---

## Advantages

✓ **Available everywhere** - Works in any project
✓ **Quick invocation** - Just `/refine` or `/expand`
✓ **Context-aware** - Can detect content type
✓ **No duplication** - Single source in quill/
✓ **Easy updates** - Update quill/, skill uses latest

---

## Integration with Other Tools

### With fis:

**Use fis for:** Story-aware generation (knows characters, world, themes)
**Use Quill for:** Quick polish, journal entries, non-fiction

```bash
# In fis project:
/fis-pipeline chapter3  # Uses fis's story-aware agents
/refine scene3_draft.md # Uses Quill for quick polish
```

### With Other Projects:

**Any prose anywhere:**
```bash
cd ~/any-project
/refine README.md
/expand "blog post idea: why compression follows craft"
```

---

## When to Use Skill vs. Direct Access

### Use Skill When:
- Quick refinement needed
- Working across projects
- Don't need full pipeline documentation
- Want fast `/command` access

### Use Direct (cd quill/) When:
- Learning the system
- Need to see full agent documentation
- Iterative development with multiple passes
- Want to save intermediate files

---

## Configuration

You can set defaults in `~/.claude/config.yml`:

```yaml
skills:
  quill:
    default_refine_type: fiction
    default_expand_mode: full
    quill_path: /Users/ramachandrakoganti/Desktop/code_repos/quill
```

---

## Next Steps

1. Create `~/.claude/skills/quill.md` with definition above
2. Test: `/refine` in any project
3. Optionally: Create helper script for routing
4. Use across all your writing projects
