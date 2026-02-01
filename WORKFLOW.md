# Quill Workflow Diagrams

Visual guides for using the pipeline.

---

## Basic Flow

```
┌─────────────────────┐
│   Your Raw Text     │
│  (any writing)      │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Prose Refiner      │
│  • Show not tell    │
│  • Body→emotion     │
│  • Weighted dialogue│
│  • Compress 20-30%  │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Quality Reviewer   │
│  • 10 quality checks│
│  • Specific feedback│
│  • Le Guin examples │
│  • FAIL/WEAK/OK/STRONG │
└──────────┬──────────┘
           │
           ▼
    ┌──────┴──────┐
    │             │
    ▼             ▼
Acceptable?    Needs Work?
    │             │
    │             ▼
    │     Second Pass
    │    (target issues)
    │             │
    └──────┬──────┘
           ▼
  ┌─────────────────┐
  │ Refined Text +  │
  │ Quality Review  │
  └─────────────────┘
```

---

## The Four Modes

### 1. FULL Pipeline (Recommended)

```
Input Text
    ↓
Refine (apply all 10 principles)
    ↓
Review (score against standard)
    ↓
Deliver both
```

**When to use:**
- First time with the pipeline
- Rough drafts needing work
- Want both polish + feedback

**Result:**
- Refined text (~70-80% of original length)
- Quality review with scores

---

### 2. REFINE_ONLY

```
Input Text
    ↓
Refine (apply all 10 principles)
    ↓
Deliver refined text
(skip review)
```

**When to use:**
- Quick polish needed
- Time-limited
- Already know your weak points

**Result:**
- Refined text only
- Basic stats (word count change)

---

### 3. REVIEW_ONLY

```
Input Text
    ↓
Review (score against standard)
    ↓
Deliver review
(skip refinement)
```

**When to use:**
- Already revised your text
- Want quality check
- Learning your patterns

**Result:**
- Quality review only
- Specific feedback on issues

---

### 4. ITERATIVE

```
Input Text
    ↓
Refine
    ↓
Review (identifies issues)
    ↓
Refine again (target specific issues)
    ↓
Review again (confirm improvements)
    ↓
[Optional: Third pass if needed]
    ↓
Deliver final + full history
```

**When to use:**
- Important pieces
- Want excellence, not just acceptable
- Time for multiple passes

**Result:**
- Highly polished text
- Multiple reviews showing progression

---

## Decision Tree

```
                    START
                      │
                      ▼
        ┌─────────────────────────┐
        │ What do you have?       │
        └─────────────────────────┘
                │
        ┌───────┴───────┐
        ▼               ▼
   Raw draft     Already revised
        │               │
        ▼               ▼
┌───────────────┐ ┌─────────────┐
│ How important?│ │ Want polish │
│               │ │ or feedback?│
└───────────────┘ └─────────────┘
    │                   │
    ├─High stakes   ┌───┴────┐
    │   ↓           ▼        ▼
    │ ITERATIVE   Polish  Feedback
    │               │        │
    ├─Decent draft ▼        ▼
    │   ↓       REFINE   REVIEW
    │ FULL       ONLY     ONLY
    │
    └─Time limited
        ↓
      REFINE
       ONLY
```

---

## What Each Agent Does

### Prose Refiner

```
INPUT: Raw prose
  │
  ├─▶ Find thought-reporting → Cut it
  ├─▶ Find emotion labels → Ground in body
  ├─▶ Find generic dialogue → Sharpen it
  ├─▶ Find over-explanation → Trust reader
  ├─▶ Find redundant details → Select one
  ├─▶ Find abstract language → Make concrete
  ├─▶ Find complex peaks → Simplify them
  └─▶ Compress 20-30%
      │
      ▼
OUTPUT: Refined prose
```

**Typical changes:**
- 1,000 words → 700-800 words
- "He felt anxious" → "His chest tightened"
- "I wondered if..." → "Would they...?"
- Three smells → One smell
- Long peak sentences → Short peak sentences

---

### Quality Reviewer

```
INPUT: Refined prose
  │
  ├─▶ Check 1: Show don't tell → SCORE
  ├─▶ Check 2: Body before emotion → SCORE
  ├─▶ Check 3: Weighted dialogue → SCORE
  ├─▶ Check 4: Precision under emotion → SCORE
  ├─▶ Check 5: Trust the reader → SCORE
  ├─▶ Check 6: Concrete over abstract → SCORE
  ├─▶ Check 7: Selection over catalog → SCORE
  ├─▶ Check 8: Structural variation → SCORE
  ├─▶ Check 9: Appropriate compression → SCORE
  └─▶ Check 10: POV integrity → SCORE
      │
      ├─▶ For each FAIL/WEAK:
      │   • Quote passage
      │   • Explain problem
      │   • Show Le Guin example
      │   • State fix needed
      │
      ▼
OUTPUT: Detailed review
```

**Each score:**
- FAIL = Violates principle extensively
- WEAK = Partially applied, needs improvement
- ACCEPTABLE = Meets standard adequately
- STRONG = Matches/exceeds Le Guin

---

## Iteration Pattern

### First Pass

```
Raw Draft (1,000 words)
    ↓
Prose Refiner
    ↓
Refined v1 (700 words)
    ↓
Quality Reviewer
    ↓
Scores:
✓ Show don't tell: ACCEPTABLE
✗ Body before emotion: WEAK (still some emotion labels)
✗ Weighted dialogue: FAIL (generic responses)
✓ Precision: ACCEPTABLE
✓ Trust reader: ACCEPTABLE
✓ Concrete: ACCEPTABLE
✗ Selection: WEAK (too many details)
✓ Structure: ACCEPTABLE
✓ Compression: ACCEPTABLE
✓ POV: ACCEPTABLE

Overall: NEEDS SIGNIFICANT REVISION
Issues: Dialogue, emotion grounding, detail selection
```

### Second Pass (Targeted)

```
Refined v1 (700 words)
+ Review feedback
    ↓
Prose Refiner
(Focus: dialogue, body-emotion, detail selection)
    ↓
Refined v2 (650 words)
    ↓
Quality Reviewer
    ↓
Scores:
✓ Show don't tell: ACCEPTABLE
✓ Body before emotion: ACCEPTABLE (fixed)
✓ Weighted dialogue: ACCEPTABLE (fixed)
✓ Precision: ACCEPTABLE
✓ Trust reader: ACCEPTABLE
✓ Concrete: ACCEPTABLE
✓ Selection: ACCEPTABLE (fixed)
✓ Structure: ACCEPTABLE
✓ Compression: STRONG
✓ POV: ACCEPTABLE

Overall: ACCEPTABLE
No critical issues remaining
```

**Result:** From 1,000 words of rough draft to 650 words of quality prose.

---

## Learning Cycle

```
           ┌─────────────┐
           │ Write Draft │
           └──────┬──────┘
                  │
                  ▼
           ┌─────────────┐
           │ Run Pipeline│
           └──────┬──────┘
                  │
                  ▼
        ┌──────────────────┐
        │ Study What Changed│
        └─────────┬─────────┘
                  │
                  ▼
        ┌──────────────────┐
        │ Read Le Guin     │
        │ Examples Cited   │
        └─────────┬─────────┘
                  │
                  ▼
        ┌──────────────────┐
        │ Notice Patterns  │
        │ in Your Writing  │
        └─────────┬─────────┘
                  │
                  ▼
        ┌──────────────────┐
        │ Apply Lessons    │
        │ to Next Draft    │
        └─────────┬─────────┘
                  │
                  └──────────┐
                             │
        After 5-10 cycles:   ▼
        You write refined  ┌──────────┐
        prose naturally    │ Improved │
                          │ Baseline │
                          └──────────┘
```

---

## The 10 Principles in Action

```
Your Draft                    Prose Refiner                  Refined

"I felt anxious"     ──────▶  Body before emotion  ──────▶  "Chest tightened"

"He wondered if      ──────▶  Show don't tell     ──────▶  "Would they
they would come"                                             come?"

"Yes," she said.     ──────▶  Weighted dialogue   ──────▶  "Everything's
"I don't know."                                             here," she said.

Long complex         ──────▶  Precision at        ──────▶  Short simple
peak sentence                 emotional peaks              peak sentence

"It was like a       ──────▶  Trust the reader    ──────▶  "It was a web."
web, connecting                                             (cut explanation)
everything..."

"I thought           ──────▶  Concrete over       ──────▶  "Roots in the
about belonging"              abstract                     ground. Sky above."

"Smelled of bread,   ──────▶  Selection over      ──────▶  "Smelled of
coffee, bacon,                catalog                      bread and smoke."
smoke, cinnamon"

5 sentences          ──────▶  Structural          ──────▶  Fragment. Long
starting "I was..."           variation                    sentence. Short.

300 words with       ──────▶  Appropriate         ──────▶  200 words, same
explanation                   compression                  impact, stronger

"I thought about     ──────▶  POV integrity       ──────▶  "The valley.
the valley and                                             The sea."
the sea"
```

---

## Quick Reference

### Input Checklist
- [ ] Text ready (paste or file)
- [ ] Mode chosen (FULL/REFINE/REVIEW/ITERATIVE)
- [ ] Goals clear (optional)
- [ ] Constraints noted (optional)

### Output Checklist
- [ ] Refined text received
- [ ] Quality scores reviewed
- [ ] Specific issues noted
- [ ] Le Guin examples studied
- [ ] Next steps decided

### Quality Targets
- **First draft:** Aim for mostly ACCEPTABLE
- **Important pieces:** Aim for mostly STRONG
- **Learning:** Focus on your weakest scores

### Iteration Guide
- **1 pass:** Quick polish, decent drafts
- **2 passes:** Rough drafts to acceptable
- **3 passes:** Acceptable to strong
- **More than 3:** Structural issues, manual revision needed

---

## That's the workflow!

Simple flow: Text → Refine → Review → Result

Complex needs: Iterate with targeted focus

Learning goal: Study changes, internalize principles

Start with QUICKSTART.md and dive in.
