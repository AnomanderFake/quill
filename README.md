# Quill: Complete Writing Pipeline System

A dual-pipeline writing system inspired by Ursula K. Le Guin's literary mastery. **Generate** prose from ideas, **refine** existing prose, or chain both together for complete authorship assistance.

---

## What This Is

**Quill** is a modular writing system with two complementary pipelines:

### 🌱 Expansion Pipeline
**Generate prose from ideas**
- Turn concepts into structured beats
- Create Le Guin-quality draft prose
- Work from loose thoughts to complete scenes

### ✨ Refinement Pipeline
**Polish existing prose**
- Apply Le Guin's 10 principles
- Compress and strengthen (typically -20-40%)
- Expand depth strategically (+15-25% enrichment)
- Get quality assessment with specific feedback

### 🎯 Master Orchestrator
**Intelligent routing**
- Detects what you have (idea vs. prose)
- Routes to appropriate pipeline(s)
- Chains pipelines when needed

---

## Quick Start

### Option 1: Let the System Decide (Recommended)

**Just paste your content** - idea, beats, or prose:

```
[Your content here]
```

The **Master Orchestrator** detects what you have and routes appropriately:
- **Idea?** → Expansion Pipeline
- **Raw prose?** → Refinement Pipeline
- **Want both?** → Expansion → Refinement

### Option 2: Choose Your Pipeline

**Have an idea? Want prose?**
→ Use Expansion Pipeline (`agents/expansion/expansion_coordinator.md`)

**Have prose? Want polish?**
→ Use Refinement Pipeline (`agents/refinement/refinement_coordinator.md`)

**Not sure?**
→ Use Master Orchestrator (`agents/master_orchestrator.md`)

---

## The Two Pipelines

### Expansion Pipeline: Idea → Prose

```
Your Idea/Thoughts/Beats
    ↓
Idea Expander (creates structured beats)
    ↓
Prose Generator (creates Le Guin-quality draft)
    ↓
Draft Prose (800-1200 words typical)
```

**What it does:**
- Converts loose ideas into structured beats
- Identifies key images and emotional arcs
- Generates prose that already shows (doesn't tell)
- Applies Le Guin principles during generation

**When to use:**
- You have an idea, need prose
- Plotting a scene
- Journal thoughts → full entry
- Exploring concepts through writing

**See:** `workflows/expand_only.md`

---

### Refinement Pipeline: Prose → Polish

```
Your Prose (raw draft)
    ↓
Prose Refiner (applies 10 Le Guin principles)
    ↓
Quality Reviewer (assesses against standard)
    ↓
Refined Prose + Quality Review
```

**What it does:**
- Shows instead of tells
- Grounds emotion in body
- Weighs dialogue
- Compresses (typically 20-30%)
- Provides quality scores and specific feedback

**When to use:**
- You have prose, need polish
- Tighten journal entries
- Strengthen drafts
- Learn your craft weaknesses

**See:** `workflows/refine_only.md`

---

### Depth Expansion: Refined → Enriched

```
Refined Prose (compressed)
    ↓
Depth Expander (adds strategic depth)
    ↓
Enriched Prose (+15-25% breathing room)
```

**What it does:**
- Adds sensory grounding to key moments
- Deepens emotional peaks
- Smooths transitions
- Lets moments breathe
- Maintains Le Guin quality

**When to use:**
- Refined prose feels too skeletal
- Emotional moments need more space
- For publication (needs richness)
- Quality reviewer noted "thin spots"

**See:** `workflows/expand_depth.md`

---

### Combined: Idea → Finished Prose

```
Your Idea
    ↓
Expansion Pipeline (generates prose)
    ↓
Refinement Pipeline (polishes prose)
    ↓
Finished Prose + Quality Review
```

**Complete journey:** Concept to publication-ready in one workflow

**See:** `workflows/expand_then_refine.md`

---

## The 10 Principles (Applied in Both Pipelines)

1. **Show, don't tell** - Cut thought-reporting, trust images
2. **Body before emotion** - "Chest tightened" not "felt anxious"
3. **Weighted dialogue** - Every line does multiple jobs
4. **Precision under emotion** - Simplify at peaks
5. **Trust the reader** - Don't explain metaphors
6. **Concrete over abstract** - Things, not concepts
7. **Selection over catalog** - One detail, not five
8. **Vary structure** - Break repetitive patterns
9. **Compress wisely** - Cut fat, preserve muscle
10. **Use POV** - Distance prevents self-explanation

**Expansion** applies these during generation.
**Refinement** applies these during polish.

**Result:** Le Guin-level craft throughout.

---

## Example Workflows

### Workflow 1: Generate Scene from Idea

**Input:** "Write about returning to grandmother's house after she dies"

**Process:** Expansion Pipeline
1. Idea Expander creates 7 beats
2. Prose Generator creates 850-word scene

**Output:**
- Beats showing emotional arc
- Draft scene ready to use or refine

**Time:** 15-20 minutes

---

### Workflow 2: Polish Journal Entry

**Input:** [1,000-word raw journal entry with "I felt" and "I thought"]

**Process:** Refinement Pipeline
1. Prose Refiner compresses to 680 words
2. Quality Reviewer scores: 8/10 ACCEPTABLE

**Output:**
- Refined entry (32% shorter, stronger)
- Quality review with specific feedback

**Time:** 10-15 minutes

---

### Workflow 3: Idea to Publication Quality

**Input:** "Scene where character confronts mother about past"

**Process:** Expansion → Refinement
1. Expansion generates beats + prose (920 words)
2. Refinement polishes to 650 words, scores ACCEPTABLE

**Output:**
- Beats
- Draft
- Refined prose
- Quality review
- Complete progression visible

**Time:** 25-35 minutes

---

## File Structure

```
quill/
├── README.md (this file)
├── QUICKSTART.md (get started in 3 steps)
│
├── agents/
│   ├── expansion/
│   │   ├── idea_expander.md (beats from ideas)
│   │   ├── prose_generator.md (prose from beats)
│   │   └── expansion_coordinator.md (orchestrates expansion)
│   │
│   ├── refinement/
│   │   ├── prose_refiner.md (line-level polish)
│   │   ├── depth_expander.md (strategic enrichment)
│   │   ├── quality_reviewer.md (assessment)
│   │   └── refinement_coordinator.md (orchestrates refinement)
│   │
│   └── master_orchestrator.md (intelligent routing)
│
├── workflows/
│   ├── expand_only.md (generation workflow)
│   ├── refine_only.md (polish workflow)
│   ├── expand_depth.md (depth enrichment workflow)
│   ├── expand_then_refine.md (complete pipeline)
│   └── iterative_development.md (multiple cycles)
│
├── guides/
│   ├── refinement_guide.md (10 principles)
│   └── first_person_guide.md (POV-specific guidance)
│
├── integration/
│   ├── SKILL_SETUP.md (use as Claude Code skill)
│   ├── FIS_INTEGRATION.md (integrate with fis project)
│   ├── INTEGRATION_OPTIONS.md (all integration methods)
│   └── DEPLOYMENT.md (current deployment status)
│
└── resources/
    ├── examples_earthsea (Le Guin benchmark)
    └── examples_dispossessed (Le Guin benchmark)
```

---

## Usage Patterns

### Pattern 1: Quick Generation
**Need:** Prose from idea
**Use:** Expansion only
**Time:** 15-20 min
**Output:** Draft prose

### Pattern 2: Quick Polish
**Need:** Tighten existing prose
**Use:** Refinement only
**Time:** 10-15 min
**Output:** Refined + review

### Pattern 3: Complete Pipeline
**Need:** Idea to finished prose
**Use:** Expansion → Refinement
**Time:** 25-35 min
**Output:** Full progression

### Pattern 4: Iterative Development
**Need:** Perfect important work
**Use:** Multiple cycles
**Time:** 40-60 min
**Output:** Excellence

---

## What Makes This Different

### vs. Traditional "First Draft" Tools
**Traditional:** Generate everything, fix later
**Quill Expansion:** Generate with principles embedded

### vs. Traditional "Editing" Tools
**Traditional:** Grammar and spelling
**Quill Refinement:** Literary craft and emotional truth

### vs. Generic AI Writing
**Generic:** Any style, variable quality
**Quill:** Le Guin standard, consistent quality

---

## Getting Started

### Step 1: Read Quick Start
- `QUICKSTART.md` (3 steps to get running)
- `guides/refinement_guide.md` (10 principles reference)

### Step 2: Choose a Workflow
- Have idea? → `workflows/expand_only.md`
- Have prose? → `workflows/refine_only.md`
- Want both? → `workflows/expand_then_refine.md`
- Not sure? → Use Master Orchestrator

### Step 3: Try It
Pick one:
- Generate scene from idea (try expansion)
- Polish journal entry (try refinement)
- Complete pipeline (try both)

### Step 4: Study Results
- What changed?
- Why did it change?
- What can you learn?

### Step 5: Set Up Integration (Optional)
- As skill: `integration/SKILL_SETUP.md` (use `/refine`, `/expand`, `/review` everywhere)
- With fis: `integration/FIS_INTEGRATION.md`
- Other options: `integration/INTEGRATION_OPTIONS.md`

---

## Advanced Usage

### Combine Pipelines Creatively

**Generate variations:**
- Same idea, different beats → Multiple versions
- Compare generated options → Pick best

**Targeted generation:**
- Generate just one scene beat
- Insert into existing work

**Iterative refinement:**
- First pass: General polish
- Second pass: Target specific issues (dialogue, emotion)
- Third pass: Final perfection

### Build a Project

```
project/
├── ideas/ (raw concepts)
├── beats/ (expanded structures)
├── drafts/ (generated prose)
├── refined/ (polished versions)
└── final/ (ready for use)
```

Track progression from idea to finish.

---

## For Different Use Cases

### Fiction Writers
- Plot scenes → Generate → Refine → Integrate
- Multiple POV handling (first and third person)
- Chapter-level iteration

### Journal Writers
- Thoughts → Structure → Polish → Reflect
- First-person optimization (see `guides/first_person_guide.md`)
- Quick daily polish

### Essayists
- Thesis → Beats → Prose → Publication quality
- Intellectual content grounded physically
- Compression for word limits

### Memoirists
- Memory fragments → Scene → Refined memory
- Show-not-tell especially critical
- Physical detail over analysis

---

## Learning from the Pipeline

### What You'll Learn

**From Expansion:**
- How ideas become structure (beats)
- What makes a moment "beat-worthy"
- Physical grounding techniques
- Emotional arc construction

**From Refinement:**
- Your specific weaknesses (quality scores)
- How to show instead of tell
- Compression without loss
- Le Guin's techniques in practice

**From Both:**
- Complete authorship process
- How craft decisions compound
- What "Le Guin quality" means

### Track Your Progress

After 10 runs through pipelines:
- Notice your patterns (always WEAK on dialogue?)
- See improvement (scores rising?)
- Internalize principles (writing refined prose naturally?)

---

## Philosophy

This system embodies a belief:

**Great prose isn't about beautiful language. It's about invisible craft that lets readers experience the story directly.**

Le Guin's prose disappears. You don't notice the writing—you notice the character's cold hands, the smell of smoke, the weight of a decision.

**Expansion Pipeline teaches:** How to build that invisible craft from the start

**Refinement Pipeline teaches:** How to remove what blocks direct experience

**Both teach:** Writing with Le Guin's level of mastery

---

## Version

**v2.1** — Depth expansion capability
- Added: Depth Expander agent (strategic enrichment +15-25%)
- Added: EXPAND_DEPTH mode in Refinement Coordinator
- Added: `workflows/expand_depth.md`
- Fills gap between compression and generation
- Adapted from fis Second Draft Agent (made generic)

**v2.0** — Dual-pipeline system
- Added: Complete expansion pipeline (Idea Expander, Prose Generator)
- Added: Master Orchestrator for intelligent routing
- Added: Workflow documentation
- Restructured: Modular agent organization
- Enhanced: First-person support

**v1.0** — Refinement pipeline only

---

## Next Steps

1. **Read `QUICKSTART.md`** - Get running in 5 minutes
2. **Try one workflow** - Pick from `workflows/`
3. **Study what changes** - Learn from before/after
4. **Apply lessons** - Write with principles in mind
5. **Iterate** - Build mastery through practice

---

## Questions?

**"Which pipeline do I need?"**
→ Use Master Orchestrator—it detects and routes

**"Can I use just one pipeline?"**
→ Yes! Each works independently

**"How do I get Le Guin-level quality?"**
→ Use full pipeline (Expansion → Refinement)

**"Does this work for [my genre]?"**
→ Principles apply across all prose

**"Can I customize the process?"**
→ Yes—agents are modular, workflows are flexible

---

Start with `QUICKSTART.md` or dive into a workflow.

The system is ready. Write something.
