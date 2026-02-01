# Quill Integration Documentation

How to use Quill across projects and integrate with other systems.

---

## Files in This Directory

### [SKILL_SETUP.md](SKILL_SETUP.md) ⭐ Recommended

Set up Quill as a Claude Code skill for system-wide access.

**What you get:**
- `/refine` - Refine prose from anywhere
- `/expand` - Generate prose from ideas
- `/review` - Quality check prose

**Setup time:** 2 minutes

---

### [FIS_INTEGRATION.md](FIS_INTEGRATION.md)

How Quill complements the fis story pipeline.

**Current status:** ✓ Deployed (fis v2.1 uses Quill for refinement)

**Contents:**
- Integration strategies
- Comparison: fis vs Quill
- When to use which
- Implementation details

---

### [INTEGRATION_OPTIONS.md](INTEGRATION_OPTIONS.md)

Complete guide to all integration methods.

**Covers:**
- Skill (recommended)
- Symlink
- Git Submodule
- Environment Variable
- Direct Path Reference
- Copy (not recommended)

**Includes:** Decision matrix, pros/cons, migration paths

---

### [DEPLOYMENT.md](DEPLOYMENT.md)

Current deployment status and architecture.

**Documents:**
- Skill deployment (status: ✓ deployed)
- fis integration (status: ✓ deployed)
- Usage patterns
- File structure
- Testing status
- Next steps

---

## Quick Decision Guide

**Want to use Quill from anywhere?**
→ [SKILL_SETUP.md](SKILL_SETUP.md)

**Working on fis project?**
→ [FIS_INTEGRATION.md](FIS_INTEGRATION.md) (already integrated as of v2.1)

**Need to integrate with another project?**
→ [INTEGRATION_OPTIONS.md](INTEGRATION_OPTIONS.md)

**Want to see current deployment status?**
→ [DEPLOYMENT.md](DEPLOYMENT.md)

---

## Integration Summary

### ✓ Deployed Integrations

1. **Claude Code Skill**
   - Location: `~/.claude/skills/quill.md`
   - Commands: `/refine`, `/expand`, `/review`
   - Available everywhere

2. **fis Pipeline (v2.1)**
   - Location: `../fis/agents/pipeline_coordinator_agent.md`
   - Stages 3 & 6 route to Quill refinement
   - Maintains story context while using Quill craft

---

## Support

**For skill issues:**
- Check `~/.claude/skills/quill.md` exists
- Verify commands: `/refine`, `/expand`, `/review`

**For fis integration issues:**
- Check `../fis/agents/pipeline_coordinator_agent.md` (should be v2.1)
- Verify path: `../quill/agents/refinement/refinement_coordinator.md`

**For other integration questions:**
- Read [INTEGRATION_OPTIONS.md](INTEGRATION_OPTIONS.md)
- Check examples for your use case
