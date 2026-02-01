# All Integration Options

## Quick Decision Matrix

| Method | Best For | Ease | Flexibility |
|--------|----------|------|-------------|
| **Skill** ⭐ | Daily use, any project | Easy | High |
| **Symlink** | Quick access from other repos | Easy | Medium |
| **Git Submodule** | Version control integration | Medium | High |
| **Direct Reference** | Simple, no setup | Very Easy | Low |
| **Environment Variable** | System-wide access | Easy | High |

---

## Option 1: Skill (RECOMMENDED)

**Best for:** Daily writing workflow across projects

### Setup:
```bash
# Create skill definition
mkdir -p ~/.claude/skills
cp quill/SKILL_SETUP.md ~/.claude/skills/quill.md

# Use from anywhere
cd ~/any-project
/refine
/expand
/review
```

### Pros:
✓ Works everywhere
✓ Quick `/command` invocation
✓ No repo duplication
✓ Easy updates (edit quill/, skill uses latest)

### Cons:
✗ Requires skill system setup
✗ Less obvious to collaborators

---

## Option 2: Symlink

**Best for:** Quick access from other projects

### Setup:
```bash
# In another project (e.g., fis)
cd ~/code_repos/fis
ln -s ../quill/agents ./quill-agents

# Now accessible
ls quill-agents/
# → expansion/ refinement/ master_orchestrator.md
```

### Usage:
```bash
# From fis
cd ~/code_repos/fis

# Reference Quill agents
cat quill-agents/refinement/prose_refiner.md
```

### Pros:
✓ Simple setup
✓ Always up-to-date (symlink tracks source)
✓ Visible in project structure
✓ Works with git (symlink committed, not content)

### Cons:
✗ Relative path dependencies
✗ Doesn't work if repos move

---

## Option 3: Git Submodule

**Best for:** Projects under version control

### Setup:
```bash
# In another repo (e.g., fis)
cd ~/code_repos/fis
git submodule add ../quill tools/quill

# Clone repo with submodules
git clone --recursive [repo-url]

# Or initialize after clone
git submodule update --init --recursive
```

### Usage:
```bash
# Quill appears as subdirectory
ls tools/quill/
# → agents/ workflows/ guides/

# Reference agents
cat tools/quill/agents/refinement/prose_refiner.md

# Update quill to latest
cd tools/quill
git pull origin main
cd ../..
git add tools/quill
git commit -m "Update quill submodule"
```

### Pros:
✓ Version-controlled reference
✓ Pin to specific quill version
✓ Update when ready (not forced)
✓ Works with teams (everyone gets it)

### Cons:
✗ More complex git workflow
✗ Can get out of sync
✗ Requires submodule knowledge

---

## Option 4: Environment Variable

**Best for:** System-wide access via scripts

### Setup:
```bash
# Add to ~/.zshrc or ~/.bashrc
export QUILL_PATH="$HOME/code_repos/quill"

# Create helper functions
quill_refine() {
  cat "$QUILL_PATH/agents/refinement/refinement_coordinator.md"
}

quill_expand() {
  cat "$QUILL_PATH/agents/expansion/expansion_coordinator.md"
}

quill_review() {
  cat "$QUILL_PATH/agents/refinement/quality_reviewer.md"
}

# Reload shell
source ~/.zshrc
```

### Usage:
```bash
# From anywhere
cd ~/any-project
echo $QUILL_PATH
# → /Users/.../quill

quill_refine
# → Shows refinement agent
```

### Pros:
✓ System-wide access
✓ Works in all shells
✓ No project-specific setup

### Cons:
✗ Requires shell configuration
✗ Less discoverable
✗ Harder for collaborators

---

## Option 5: Direct Path Reference

**Best for:** Simple, one-time usage

### Setup:
None! Just reference the path.

### Usage:
```bash
# From any project
cat ~/code_repos/quill/agents/refinement/prose_refiner.md

# Or create alias
alias quill="cd ~/code_repos/quill"
```

### Pros:
✓ Zero setup
✓ Explicit and clear
✓ Works immediately

### Cons:
✗ Long paths every time
✗ Not portable
✗ Tedious for frequent use

---

## Option 6: Copy Agents (NOT RECOMMENDED)

**Don't do this unless necessary.**

### Why Not:
✗ Duplication = maintenance nightmare
✗ Updates don't propagate
✗ Version drift
✗ Hard to track which is current

### Only Use If:
- Need to customize heavily for specific project
- Forking intentionally
- One-time extraction

---

## Comparison

### For fis Integration:

**Best: Skill**
- Available in fis and everywhere else
- No fis code changes
- Quick access

**Alternative: Symlink**
- `fis/quill-agents/` visible in project
- Good for reference
- Easy setup

**Alternative: Submodule**
- If fis is in git
- Want version control
- Working with others

---

### For System-Wide Use:

**Best: Skill**
- Works everywhere
- `/command` invocation
- Professional

**Alternative: Environment Variable**
- Good for scripts
- Shell-level access

---

### For Learning/Development:

**Best: Direct Path**
- Simple
- Explicit
- No magic

---

## Recommended Setup

### 1. Make Quill a Skill (Primary)
Follow `SKILL_SETUP.md`

### 2. Add Environment Variable (Backup)
```bash
echo 'export QUILL_PATH="$HOME/code_repos/quill"' >> ~/.zshrc
```

### 3. Use Directly When Needed
```bash
cd ~/code_repos/quill
# Work here for development/learning
```

### Result:
- Skill for daily use
- Env var for scripting
- Direct access for deep work

---

## Example: Using All Three

```bash
# Daily writing workflow (Skill)
cd ~/Documents/journal
/refine today.md --type=journal

# Script to batch process (Env var)
for file in *.md; do
  cat "$QUILL_PATH/agents/refinement/prose_refiner.md"
  # Process $file
done

# Learning/customization (Direct)
cd ~/code_repos/quill
# Edit agents, test changes
```

---

## Migration Path

### Starting Point: Direct Use
```bash
cd ~/code_repos/quill
# Use agents directly
```

### Add Convenience: Environment Variable
```bash
export QUILL_PATH="$HOME/code_repos/quill"
# Now reference from anywhere
```

### Full Integration: Skill
```bash
# Install as skill
# Now /refine works everywhere
```

**You can use all three!** They're not exclusive.

---

## For Collaboration

### If Sharing with Others:

**Option A: Skill** (Recommended)
- Include skill definition in project docs
- Easy for others to install
- No repo changes needed

**Option B: Submodule**
- Quill bundled with project
- Everyone gets it automatically
- Version controlled

**Option C: Documentation**
- "Install Quill from github.com/..."
- Point to installation instructions
- Let each person choose method

---

## Summary

**Recommended approach:**

1. **Install Quill as a Skill** (`SKILL_SETUP.md`)
   - Use from anywhere with `/refine`, `/expand`, `/review`

2. **Add QUILL_PATH to shell config** (optional)
   - For scripting and automation

3. **Keep quill repo separate**
   - Update in one place
   - Benefits all uses

**For fis specifically:**
- Skill approach (use alongside fis)
- No changes to fis codebase
- Complementary tools

**Next step:** Follow `SKILL_SETUP.md` to set up skill.
