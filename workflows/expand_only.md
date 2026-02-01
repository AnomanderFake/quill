# Workflow: Expansion Only

Generate prose from ideas without refinement.

---

## When to Use

- You have an idea, want prose generated quickly
- Draft quality is fine (will revise manually later)
- Experimenting with different approaches
- Learning how ideas become prose

---

## Process

```
Your Idea
    ↓
Idea Expander (converts to beats)
    ↓
Prose Generator (creates draft)
    ↓
Draft Prose → You
```

**Time:** Single pass
**Output:** Beats + Draft prose (800-1200 words typical)

---

## Step by Step

### 1. Prepare Your Idea

Can be:
- Loose concept ("write about returning home")
- Plot point ("character confronts mother")
- Journal thought ("feeling displaced in familiar place")
- Scene concept ("first morning of freedom")

**Don't need:**
- Full outline
- Character details
- Structured beats (that's what Idea Expander creates)

### 2. Use Expansion Coordinator

Mode: **FULL** (or let Master Orchestrator detect)

Provide:
```
## Input
[Your idea]

## Mode
FULL (Expansion only, no refinement)

## Optional Context
- POV preference (first or third)
- Length target
- Must-include elements
```

### 3. Review Beats

**You'll receive:** Structured beats showing:
- Sequence of moments
- Emotional arc
- Key images
- Sensory anchors

**Check:** Do these beats match your vision?

**If yes:** Continue to prose generation
**If no:** Request beat revision (see Iterative workflow)

### 4. Receive Draft Prose

**Prose Generator creates draft that already:**
- Shows, doesn't tell
- Grounds emotion in body
- Uses weighted dialogue
- Applies Le Guin principles

**Better than typical first draft** (but still draftquality)

### 5. Decide Next Steps

Options:
- ✓ **Accept as-is** - Use the draft
- ✓ **Refine** - Run through Refinement Pipeline
- ✓ **Iterate** - Revise beats, regenerate
- ✓ **Manual revision** - Edit yourself

---

## Example

**Input:**
"Write about a character returning to their grandmother's house after she dies, realizing the place isn't home anymore—she was."

**Expansion Coordinator generates:**

**Beats (7 total):**
1. Arrival: Key under stone (brief)
2. Entry: Kitchen smell wrong (moderate)
3. Discovery: Mending basket unfinished (PEAK)
4. Realization: House is just walls (moderate)
5. Departure: Take key, don't return it (brief)

**Prose (850 words):**
```
The key was under the third stone. Where it had always been.

[... full scene generated ...]

I locked the door. Put the key in my pocket, not back under
the stone. Walked to my car.
```

**Result:** Draft scene ready to use or refine

---

## Typical Outcomes

**Input length:** 20-100 words (just the idea)
**Beats generated:** 5-10 beats
**Prose generated:** 600-1200 words
**Quality:** Draft with Le Guin principles applied (better than raw first draft)

---

## When Expansion Only is Enough

✓ You're drafting quickly, will revise later
✓ You want to see multiple versions (generate several, pick best)
✓ You're exploring an idea, not ready for polish
✓ You're learning the expansion process
✓ Generated prose is already tight (under 800 words)

---

## When to Add Refinement

Consider refinement if:
- Generated prose >1000 words (likely needs compression)
- This is important work (publication, portfolio)
- You want Le Guin-level quality immediately
- You're not confident revising manually

See: `workflows/expand_then_refine.md`

---

## Advantages of Expansion Only

**Fast:** Single pass through one pipeline
**Flexible:** Easy to regenerate with different beats
**Educational:** See how ideas become structure become prose
**Experimental:** Try multiple approaches quickly

---

## Files You'll Receive

```
[name]_beats.md          # Structured beats
[name]_draft.md          # Generated prose
```

---

## Next Steps After Expansion

**Option A: Accept Draft**
- Use as-is in your project
- Manual revision if needed

**Option B: Refine**
- Run Refinement Pipeline
- Get polished version + quality review

**Option C: Iterate**
- Revise beats based on generated prose
- Regenerate with improved beats
- See: `workflows/iterative_development.md`

**Option D: Generate More**
- Try different beat structures
- Generate alternate versions
- Pick the best one

---

## Tips

**For best results:**
- Be specific in your idea (not just "write about loss")
- Include the core emotional truth
- Mention key images if you have them
- Note POV preference if strong opinion

**To speed up:**
- Accept first beat structure (don't overthink)
- Let Prose Generator make voice decisions
- Review prose, don't agonize over beats

**To explore:**
- Generate multiple versions from same idea
- Try different emotional arcs (beats determine this)
- Compare generated options

---

## Related Workflows

- `expand_then_refine.md` - Add polish after generation
- `iterative_development.md` - Refine beats before prose
- `refine_only.md` - Polish existing prose (skip expansion)
