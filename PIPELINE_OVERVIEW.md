# Quill Pipeline Overview

## What I Built for You

I've created a **generic writing refinement pipeline** based on your fis pipeline, but adapted to work with **any piece of prose** you input—whether it's a scene, draft, journal entry, or essay.

---

## Key Differences from fis Pipeline

### fis Pipeline (Story-Specific)

**Designed for:**
- A specific novel project
- Works on individual scenes with story context
- Requires story files (spine.md, themes.md, setting.md, characters.md, etc.)
- Multi-stage process: Story Architect → First Draft → Refine → Review → Second Draft → Refine → Review

**Agents:**
- Story Architect Agent (creates structural beats)
- First Draft Agent (generates prose from beats)
- Second Draft Agent (expands refined scenes)
- Prose Refinement Agent v1.3 (applies Le Guin techniques)
- Le Guin Standard Reviewer (quality control)
- Chapter Composer Agent (combines scenes into chapters)
- Pipeline Coordinator Agent (orchestrates all of the above)

**Strengths:**
- Complete end-to-end story generation
- Tight integration with story world and characters
- Multi-pass refinement with expansion phase

**Limitations:**
- Requires extensive story infrastructure
- Tied to a specific project
- Can't easily process arbitrary writing

---

### Quill Pipeline (Generic)

**Designed for:**
- ANY piece of writing
- No story context required
- Works with whatever you give it
- Simple process: Raw text → Refine → Review → [Optional second pass]

**Agents:**
1. **Prose Refiner** - Line-level refinement using Le Guin principles
2. **Quality Reviewer** - Assessment against literary craft standards
3. **Pipeline Coordinator** - Orchestrates the workflow

**Strengths:**
- Works with any prose input
- No infrastructure needed
- Fast and focused (just refinement and review)
- Adaptable to different genres and styles

**Use cases:**
- Polish novel scenes
- Refine personal essays
- Improve journal entries
- Tighten blog posts
- Learn craft by seeing what changes
- Quality-check your revised work

---

## What I Kept from fis

### The Core Principles

All 10 Le Guin techniques:
1. Show, don't tell
2. Body before emotion
3. Weighted dialogue
4. Precision under emotion
5. Trust the reader
6. Concrete over abstract
7. Selection over catalog
8. Structural variation
9. Appropriate compression
10. POV integrity

### The Quality Standard

Le Guin's prose as the benchmark:
- Same example chapters (Earthsea, Dispossessed)
- Same 10-point quality scoring
- Same rigorous review process
- Same specific, actionable feedback

### The Philosophy

- Refinement over generation
- Compression with depth
- Trust the reader
- Physical detail over emotion labeling
- Specific feedback with examples

---

## What I Changed

### Removed Story Dependencies

**fis requires:**
- Story spine and structure
- Character profiles
- World-building documents
- Thematic frameworks
- Scene beats from Story Architect

**Quill requires:**
- Just your text
- That's it

### Simplified the Workflow

**fis workflow (7 stages):**
```
Story Architect output (beats)
    ↓
First Draft Agent (generate prose)
    ↓
Prose Refinement Agent (first pass)
    ↓
Le Guin Reviewer (first review)
    ↓
Second Draft Agent (expansion 15-25%)
    ↓
Prose Refinement Agent (second pass)
    ↓
Le Guin Reviewer (final review)
```

**Quill workflow (2-3 stages):**
```
Your text (any writing)
    ↓
Prose Refiner (applies principles)
    ↓
Quality Reviewer (assesses quality)
    ↓
[Optional: Second refinement pass]
```

### Made It Input-Agnostic

**fis expects:**
- Scenes from a specific story
- Consistent POV (limited 3rd)
- Scene beats to work from

**Quill accepts:**
- Any prose, any genre
- Any POV (adapts to what you give it)
- Raw text without structural prep

### Focused on Refinement

**fis does:**
- Story architecture
- Prose generation
- Expansion passes
- Multi-draft management
- Chapter composition

**Quill does:**
- Prose refinement (line-level)
- Quality assessment
- Learning/improvement

It's a **refinement tool**, not a generation tool.

---

## File Structure

```
quill/
├── README.md                    # Full documentation
├── QUICKSTART.md                # Get started fast
├── PIPELINE_OVERVIEW.md         # This file
├── style_guide.md               # Quick reference (10 principles)
├── example_input.txt            # Template for your input
├── agents/
│   ├── prose_refiner.md         # Line-level refinement agent
│   ├── quality_reviewer.md      # Quality assessment agent
│   └── pipeline_coordinator.md  # Workflow orchestrator
└── resources/
    ├── examples_earthsea        # Le Guin benchmark chapter
    └── examples_dispossessed    # Le Guin benchmark chapter
```

---

## How to Use It

### Basic Workflow

1. **Prepare text** - Save as text.txt or have ready to paste
2. **Run pipeline coordinator** - Specify mode (FULL/REFINE_ONLY/REVIEW_ONLY/ITERATIVE)
3. **Receive results** - Refined text + quality review
4. **Iterate if needed** - Second pass targeting specific issues

### Example: Refining a Scene

**Input:** 1,200-word first draft of a novel scene

**Process:**
1. Use Pipeline Coordinator in FULL mode
2. Prose Refiner compresses to ~900 words, applies show-don't-tell
3. Quality Reviewer scores: Mix of ACCEPTABLE and WEAK
4. Run second pass targeting WEAK scores (dialogue, emotion grounding)
5. Final: 850 words, mostly ACCEPTABLE/STRONG

**Output:**
- `scene_refined.txt` - The polished version
- `scene_review.txt` - Quality assessment with specific feedback

### Example: Learning from Your Patterns

**Input:** Three different essays you've written

**Process:**
1. Run REVIEW_ONLY on each
2. Study the quality scores
3. Notice patterns (e.g., always WEAK on "Show, don't tell")

**Output:**
- Understanding of your craft weaknesses
- Specific examples of how to improve
- Le Guin references showing mastery

---

## Comparison Matrix

| Feature | fis Pipeline | Quill Pipeline |
|---------|--------------|----------------|
| **Input** | Story beats, scene outlines | Any prose text |
| **Dependencies** | Story files required | None |
| **Stages** | 7 (Architect→Draft→Refine→Review→Expand→Refine→Review) | 2-3 (Refine→Review→[Optional second pass]) |
| **Generates prose** | Yes (First Draft, Second Draft agents) | No (refinement only) |
| **Refines prose** | Yes (Prose Refinement agent, 2x per scene) | Yes (Prose Refiner) |
| **Quality control** | Yes (Le Guin Reviewer, 2x per scene) | Yes (Quality Reviewer) |
| **Story-aware** | Yes (knows characters, world, themes) | No (generic) |
| **Genre-specific** | Literary fiction in Le Guin style | Any genre, any style |
| **POV handling** | Limited 3rd with distance (prescribed) | Adapts to input POV |
| **Expansion phase** | Yes (Second Draft agent adds 15-25%) | No (compression focused) |
| **Use case** | Generate and refine complete novel | Refine any writing, learn craft |

---

## When to Use Which

### Use fis Pipeline When:
- You're writing a novel with established world/characters
- You need prose generated from structural beats
- You want multi-pass refinement with expansion
- You're committed to Le Guin-style limited 3rd POV
- You need story-aware refinement (character voice consistency, thematic echoes)

### Use Quill Pipeline When:
- You have prose that needs refinement
- You're working across multiple projects
- You want to learn craft principles
- You need quick polish on essays, journal entries, etc.
- You want quality assessment without story context
- You're experimenting with different genres/styles

---

## Extending Quill

The pipeline is modular. You can:

### Add Agents

Create new agents in `agents/`:
- `dialogue_specialist.md` - Focus only on dialogue
- `description_refiner.md` - Polish sensory details
- `pacing_analyzer.md` - Check rhythm and flow

### Customize Principles

Modify `style_guide.md` to emphasize:
- Your genre's conventions
- Your voice's signature elements
- Different quality standards

### Add Benchmarks

Add more examples in `resources/`:
- Other Le Guin chapters
- Authors you admire
- Your own best work

### Create Templates

Add templates in root for:
- Specific genres (thriller scene template, essay template)
- Common patterns (dialogue-heavy scenes, internal monologue)
- Your project structure

---

## The Philosophy Difference

### fis Pipeline
"Generate a complete novel in Le Guin's style using a structured, multi-stage process."

### Quill Pipeline
"Refine any writing to literary quality using principles derived from Le Guin's mastery."

**fis** is a **story production system**.
**Quill** is a **craft development tool**.

---

## Getting Started

1. **Read QUICKSTART.md** (5 minutes)
2. **Read style_guide.md** (10 minutes)
3. **Read one Le Guin example** (30 minutes)
4. **Try the pipeline** with 500-1000 words
5. **Study the results**
6. **Iterate**

---

## Summary

I've taken your excellent fis pipeline and distilled it into a **generic, flexible refinement system** that:

✓ Works with any prose input
✓ Requires no story infrastructure
✓ Focuses on line-level craft
✓ Teaches Le Guin's principles
✓ Provides specific, actionable feedback
✓ Adapts to your voice and style

**What you can do with it:**
- Refine novel scenes
- Polish essays
- Improve journal writing
- Learn craft systematically
- Quality-check your work
- Develop your voice

**What it won't do:**
- Generate prose from nothing
- Make structural decisions
- Replace your judgment
- Require extensive setup

It's the refinement and review core of fis, liberated to work with anything you write.

---

Start with `QUICKSTART.md` and experiment. The pipeline is a tool—use it however serves your writing best.
