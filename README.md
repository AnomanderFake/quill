# Quill: A Generic Writing Refinement Pipeline

A prose refinement system inspired by Ursula K. Le Guin's mastery of literary craft. Transform any piece of writing—scene, draft, journal entry, essay—into polished, literary-quality prose.

---

## What This Is

**Quill** is a writing pipeline that takes any prose and refines it using principles derived from studying Le Guin's work:
- Show, don't tell
- Body before emotion
- Weighted dialogue
- Precision under pressure
- Trust the reader

**What it works with:**
- Novel scenes or chapters
- Short stories
- Personal essays
- Memoir fragments
- Journal entries
- Any prose that needs refinement

**What it produces:**
- Tighter, more powerful prose (typically 20-30% shorter)
- Detailed quality assessment
- Specific revision recommendations
- Comparison to Le Guin's benchmark

---

## Quick Start

### 1. Prepare Your Text

Save your writing as `text.txt` (or any filename) in this directory.

### 2. Choose Your Workflow

**Full Pipeline (Recommended):**
- Refines your prose using Le Guin principles
- Reviews it against quality standards
- Provides detailed feedback

**Refinement Only:**
- Just polishes your prose
- Skips formal review

**Review Only:**
- Assesses already-refined text
- Provides critique without changes

**Iterative:**
- Multiple passes to perfection
- For important pieces

### 3. Run the Pipeline

Use the **Pipeline Coordinator** (see `agents/pipeline_coordinator.md`) to orchestrate the workflow.

The coordinator will:
1. Take your text
2. Run it through the Prose Refiner
3. Run it through the Quality Reviewer
4. Deliver refined text + quality report

### 4. Review Results

You'll receive:
- **Refined text** - Tightened, showing increased, telling reduced
- **Quality review** - 10-point assessment with specific feedback
- **Statistics** - Word count changes, scores, recommendations

---

## The Pipeline

```
Your text (any writing)
    ↓
Prose Refiner
    ↓
Quality Reviewer
    ↓
[Optional: Second pass if needed]
    ↓
Refined text + Review → You
```

### Prose Refiner

Applies 10 core principles to any prose:

1. **Show, don't tell** - Cuts thought-reporting, trusts images
2. **Body before emotion** - Grounds feeling in sensation
3. **Weighted dialogue** - Makes every line do multiple jobs
4. **Precision under emotion** - Simplifies at peaks
5. **Trust the reader** - No explaining metaphors
6. **Concrete over abstract** - Physical reality over concepts
7. **Selection over catalog** - One detail, not five
8. **Vary structure** - Breaks repetitive patterns
9. **Compress wisely** - Cuts fat, keeps muscle
10. **Let POV work** - Uses distance productively

**Typical results:**
- 20-30% compression
- Stronger emotional impact
- Cleaner, more precise language
- Dialogue that reveals character

See: `agents/prose_refiner.md`

### Quality Reviewer

Assesses refined prose against Le Guin's standard:

Scores 10 quality checks:
- Show, don't tell
- Body before emotion
- Weighted dialogue
- Precision under emotion
- Trust the reader
- Concrete over abstract
- Selection over catalog
- Structural variation
- Appropriate compression
- POV integrity

**Each scored:** FAIL / WEAK / ACCEPTABLE / STRONG

**Provides:**
- Specific passages that need work
- Le Guin examples showing the right way
- Prioritized revision recommendations
- Comparison to benchmark

See: `agents/quality_reviewer.md`

---

## Example Workflow

### Example 1: Draft Scene → Polished Scene

**Input:** 1,500-word first draft of a novel scene

**Process:**
1. Run Full Pipeline
2. Prose Refiner compresses to 1,100 words
3. Quality Reviewer scores: Mix of ACCEPTABLE and WEAK
4. Run second refinement pass targeting specific issues
5. Second review: Mostly ACCEPTABLE/STRONG

**Result:** 1,050-word refined scene meeting quality standards

**Time:** Two passes

---

### Example 2: Personal Essay Polish

**Input:** 800-word essay, already decent

**Process:**
1. Run Refinement Only (quick polish)
2. Output: 650 words, tighter and stronger

**Result:** 19% compression, cleaner prose

**Time:** Single pass

---

### Example 3: Quality Check

**Input:** Short story you've already revised

**Process:**
1. Run Review Only
2. Get detailed assessment

**Result:** Specific feedback on dialogue, emotion grounding, compression opportunities

**Time:** Single pass

---

## The Benchmark: Le Guin's Work

This pipeline uses two chapters as reference standards:

### A Wizard of Earthsea - Chapter 1
- Covers birth to age 13 in ~6,000 words
- Demonstrates: Fragments representing years, show-not-tell, physical emotion
- Study for: Childhood narratives, compression, sensory grounding

### The Dispossessed - Chapter 1
- Covers age 2 to 20 in ~12,000 words
- Demonstrates: Vivid scenes as phases, weighted dialogue, concrete philosophy
- Study for: Life-span narratives, intellectual content grounded physically

Both available in `resources/`

These aren't meant to force your writing to sound like Le Guin. They're examples of **craft mastery**—how to show without telling, ground emotion in body, make dialogue do multiple jobs, trust your reader.

---

## File Structure

```
quill/
├── README.md (this file)
├── style_guide.md (quick reference)
├── agents/
│   ├── prose_refiner.md (line-level refinement)
│   ├── quality_reviewer.md (assessment against standard)
│   └── pipeline_coordinator.md (workflow orchestration)
└── resources/
    ├── examples_earthsea (Le Guin chapter 1)
    └── examples_dispossessed (Le Guin chapter 1)
```

---

## Usage Patterns

### Pattern 1: Rough Draft → Publication-Ready

**For:** First drafts with common issues

**Workflow:** FULL pipeline, likely 2 passes

**What happens:**
- First pass: Major tightening, showing increased, 30-40% reduction
- Review: Identifies remaining weaknesses
- Second pass: Targeted fixes
- Final: Meets ACCEPTABLE standard or higher

**When to use:** Important writing you want to perfect

---

### Pattern 2: Quick Polish

**For:** Decent drafts that just need tightening

**Workflow:** REFINE_ONLY

**What happens:**
- Single refinement pass
- 20-30% compression
- Cleaner prose

**When to use:** Good enough drafts, time-limited, routine polishing

---

### Pattern 3: Learning Tool

**For:** Understanding your craft weaknesses

**Workflow:** REVIEW_ONLY on your revised drafts

**What happens:**
- Detailed assessment
- Specific examples of what to improve
- Le Guin comparisons showing better approaches

**When to use:** Skill development, understanding your patterns

---

### Pattern 4: Iterative Perfection

**For:** Critical pieces (opening chapter, key scenes, published essays)

**Workflow:** ITERATIVE, 2-3 passes

**What happens:**
- First refinement + review
- Targeted second refinement on weak areas
- Second review confirming improvements
- Optional third pass if needed

**When to use:** Stakes are high, quality must be excellent

---

## What This Pipeline Does Well

✓ **Tightens prose** - Removes over-explanation, cuts telling
✓ **Sharpens dialogue** - Makes every line do work
✓ **Grounds emotion** - Converts feelings to physical sensations
✓ **Increases precision** - Simplifies at emotional peaks
✓ **Provides specific feedback** - Not vague "could be better"
✓ **Shows examples** - Le Guin comparisons for every issue
✓ **Adapts to your voice** - Doesn't impose Le Guin's style, uses her principles

---

## What This Pipeline Doesn't Do

✗ **Generate new content** - It refines what you give it
✗ **Fix structure** - Plot, pacing, organization need manual work
✗ **Change genre** - Sci-fi stays sci-fi, memoir stays memoir
✗ **Replace your judgment** - You decide what feedback to accept
✗ **Work on poetry** - Different craft entirely

---

## Common Questions

### "Will this make my writing sound like Le Guin?"

No. It will make your writing **clearer, tighter, and more emotionally resonant** using principles she mastered. Your voice remains yours.

### "What if I'm writing genre fiction, not literary fiction?"

The principles work across genres:
- Show-not-tell applies to thrillers
- Weighted dialogue applies to romance
- Body-before-emotion applies to sci-fi

Le Guin herself wrote across genres (fantasy, sci-fi, realistic fiction).

### "How much compression should I expect?"

Typical: 20-30% reduction on first pass.

But the goal isn't shortness—it's **impact**. Sometimes a scene gains words by adding necessary sensory detail or emotional beats.

### "What if the Quality Reviewer fails my writing?"

FAIL scores mean specific, fixable issues:
- Thought-reporting present (cut it)
- Generic dialogue (sharpen it)
- Emotions not grounded (add physical sensation)

Each FAIL comes with examples and revision guidance.

### "How many passes do I need?"

- **Decent drafts:** 1 pass
- **Rough drafts:** 2 passes
- **Important pieces:** 2-3 passes
- **If still failing after 3:** May need structural work, not line-level refinement

---

## Tips for Best Results

### Before Running Pipeline

1. **Know what you're refining** - Scene? Essay? Journal entry?
2. **Set goals** - What do you want improved?
3. **Note constraints** - Anything to preserve?

### During Pipeline

1. **Read the quality review carefully** - Don't just look at scores
2. **Study the Le Guin examples provided** - See how she handled similar moments
3. **Focus second passes** - Target specific issues, not general re-refinement

### After Pipeline

1. **Don't accept everything blindly** - You're the final judge
2. **Learn from patterns** - Do you over-explain? Use generic dialogue?
3. **Apply lessons to new writing** - Internalize the principles

---

## Advanced Usage

### For Ongoing Projects

Create a `drafts/` folder:
- `scene01_draft.txt` → `scene01_refined.txt` + `scene01_review.txt`
- `scene02_draft.txt` → `scene02_refined.txt` + `scene02_review.txt`

Track your quality scores over time. Are you improving?

### For Learning

Run Review Only on published authors you admire:
- How do they score against Le Guin standard?
- What techniques do they use?
- What could be tighter?

### For Specific Issues

Tell the Prose Refiner to focus:
- "This dialogue is generic. Make it character-specific."
- "This scene over-explains emotion. Ground it in physical sensation."
- "Too many sensory details. Select the most important."

---

## The Philosophy

This pipeline is based on one insight:

**Great prose isn't about beautiful language. It's about invisible craft that lets the reader experience the story directly.**

Le Guin's prose disappears. You don't notice the writing—you notice the character's cold hands, the smell of smoke, the weight of a decision.

That's what this pipeline teaches:
- Cut what stands between reader and experience
- Show through action and sensation
- Trust the reader's intelligence
- Make every word earn its place

Not to write like Le Guin, but to write with her level of craft.

---

## Getting Started

1. **Read the style guide** (`style_guide.md`) - Quick reference
2. **Read one Le Guin example** (`resources/examples_earthsea` or `examples_dispossessed`)
3. **Prepare a piece to refine** (500-2000 words ideal for first try)
4. **Run Full Pipeline** using Pipeline Coordinator
5. **Study the results** - Refined text + quality review
6. **Iterate if needed** - Second pass targeting specific issues

---

## Version

**v1.0** — Initial creation
**Last updated:** February 2026

---

## Acknowledgments

Built on principles derived from studying:
- *A Wizard of Earthsea* by Ursula K. Le Guin
- *The Dispossessed* by Ursula K. Le Guin

This is a teaching tool, not a replacement for reading her work. If you want to write well, read Le Guin.

---

## Questions or Issues?

This is a learning system. Experiment, adapt, make it your own.

The agents are guidelines. You're the writer.
