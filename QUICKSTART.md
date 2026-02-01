# Quick Start

Get started with Quill in 3 steps.

---

## 1. Understand What Quill Does

Read [README.md](README.md) for a complete overview of the dual-pipeline system:
- **Expansion Pipeline:** Generate prose from ideas
- **Refinement Pipeline:** Polish existing prose
- **Master Orchestrator:** Intelligent routing between pipelines

**Time:** 5-10 minutes

---

## 2. Choose Your Workflow

Pick the workflow that matches your need:

### Have an idea, want prose?
→ [workflows/expand_only.md](workflows/expand_only.md)

### Have prose, want polish?
→ [workflows/refine_only.md](workflows/refine_only.md)

### Want complete pipeline (idea → finished prose)?
→ [workflows/expand_then_refine.md](workflows/expand_then_refine.md)

### Not sure? Let the system decide
→ Use Master Orchestrator: `agents/master_orchestrator.md`

---

## 3. Try It Out

**Simplest approach:**
1. Paste your content (idea or prose)
2. Invoke the Master Orchestrator
3. It detects what you have and routes to the right pipeline
4. Review results

**Example:**
```
Your idea: "Scene where character returns to childhood home after years away"
    ↓
Master Orchestrator detects: idea
    ↓
Routes to: Expansion Pipeline
    ↓
Output: Beats + Draft prose (800-1000 words)
```

---

## Integration Options

### Use as a Claude Code Skill (Recommended)

Follow [integration/SKILL_SETUP.md](integration/SKILL_SETUP.md) to set up `/refine`, `/expand`, `/review` commands available everywhere.

### Integrate with Other Projects

- **For fis project:** [integration/FIS_INTEGRATION.md](integration/FIS_INTEGRATION.md)
- **All integration options:** [integration/INTEGRATION_OPTIONS.md](integration/INTEGRATION_OPTIONS.md)
- **Current deployment status:** [integration/DEPLOYMENT.md](integration/DEPLOYMENT.md)

---

## Learning Resources

- **10 Principles:** [guides/refinement_guide.md](guides/refinement_guide.md)
- **First-person/journals:** [guides/first_person_guide.md](guides/first_person_guide.md)
- **Le Guin examples:** [resources/examples_earthsea](resources/examples_earthsea), [resources/examples_dispossessed](resources/examples_dispossessed)

---

## Quick Reference

### File Structure
```
agents/
├── expansion/          # Generate prose from ideas
├── refinement/         # Polish existing prose
└── master_orchestrator.md  # Intelligent routing

workflows/              # Specific workflow guides
guides/                 # Principle references
integration/            # Setup and integration docs
resources/              # Le Guin examples
```

### Common Questions

**"Which pipeline do I need?"**
→ Use Master Orchestrator—it detects and routes automatically

**"Can I use just one pipeline?"**
→ Yes! Each works independently

**"How do I use this in other projects?"**
→ See [integration/SKILL_SETUP.md](integration/SKILL_SETUP.md)

**"What quality can I expect?"**
→ Le Guin-level craft application (see Le Guin examples in resources/)

---

That's it. Start with [README.md](README.md) for complete details, or jump to [workflows/](workflows/) to try a specific workflow.
