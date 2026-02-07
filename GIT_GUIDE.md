# Git Cheat Sheet for Designers

## The Mental Model

Git is version control. Think of it like:
- **Time machine** for your files
- **Infinite undo** with labels
- **Collaboration** without "final_final_v3.html"

## Your Workflow (Visual)

```
1. MAKE CHANGES          2. STAGE THEM           3. COMMIT              4. PUSH TO CLOUD
   (Edit files)             (git add)               (git commit)            (git push)

   ┌─────────┐            ┌─────────┐            ┌─────────┐            ┌─────────┐
   │  index  │            │  index  │            │ Snapshot│            │ GitHub  │
   │  .html  │──────────▶ │  .html  │──────────▶ │ "Fixed  │──────────▶ │ ☁️      │
   │         │            │    ✓    │            │  nav"   │            │         │
   └─────────┘            └─────────┘            └─────────┘            └─────────┘
   
   Working                Staging                Local Git              Remote
   Directory              Area                   History                (GitHub)
```

## Essential Commands

### Starting a New Project

```bash
# Create a new repository
git init

# Connect to GitHub
git remote add origin https://github.com/username/repo-name.git

# First upload
git add .
git commit -m "Initial commit"
git push -u origin main
```

### Daily Workflow

```bash
# See what changed
git status

# Add changes
git add .                          # Add everything
git add index.html                 # Add specific file
git add images/                    # Add folder

# Save snapshot
git commit -m "Updated about section"

# Upload to GitHub
git push
```

### Checking Your Work

```bash
# See history
git log --oneline

# See what changed in a file
git diff index.html

# See current status
git status
```

## Command Translation

| Git Command | What It Means | Design Equivalent |
|-------------|---------------|-------------------|
| `git add .` | Mark files to save | Select layers to export |
| `git commit -m "msg"` | Save a version | Save as "Homepage_v2" |
| `git push` | Upload to cloud | Sync to Dropbox |
| `git pull` | Download latest | Get latest from shared folder |
| `git status` | What changed? | See modified layers |
| `git log` | Version history | Version history panel |
| `git diff` | Show changes | Compare versions |

## Commit Message Guide

Good commit messages help future you understand what changed:

### ❌ Bad Examples
```
git commit -m "updates"
git commit -m "fixed stuff"
git commit -m "changes"
```

### ✅ Good Examples
```
git commit -m "Added new case study for ALSA project"
git commit -m "Fixed navigation link colors for better contrast"
git commit -m "Optimized images to reduce page load time"
git commit -m "Updated contact email address"
```

### Format
```
[Action] [What] [Why (optional)]

Examples:
"Added loyalty program screenshots"
"Fixed mobile menu layout on small screens"
"Updated meta description for better SEO"
"Removed outdated blog posts"
```

## Common Scenarios

### Scenario 1: You edited your portfolio
```bash
# 1. See what changed
git status

# 2. Add the changes
git add index.html

# 3. Commit with message
git commit -m "Updated case study descriptions"

# 4. Push to GitHub
git push
```

### Scenario 2: You added new images
```bash
git add images/new-project.jpg
git commit -m "Added new project screenshots"
git push
```

### Scenario 3: You want to undo your last change (before commit)
```bash
git checkout -- index.html
# This discards changes to index.html
```

### Scenario 4: You committed but want to change the message
```bash
git commit --amend -m "New, better message"
```

## Branch Basics (Advanced)

Branches let you try things without breaking your main site:

```
       main (live site)
         │
         │
         ├──── experiment (trying new design)
         │
         │
    (merge when ready)
```

```bash
# Create new branch
git checkout -b experiment

# Work on new feature...
git add .
git commit -m "Trying new color scheme"

# Switch back to main
git checkout main

# Merge experiment into main
git merge experiment
```

## Visual Git Flow Diagram

```
YOUR EDITS                 GIT SAVES IT              GITHUB SHOWS IT
                                                    
┌──────────┐              ┌──────────┐              ┌──────────┐
│          │              │ Commit 1 │              │          │
│  Edit    │─────add─────▶│ "Added   │─────push────▶│  Live    │
│  files   │              │  nav"    │              │  site    │
│          │              │          │              │          │
└──────────┘              └──────────┘              └──────────┘
                                │                         │
                                │                         │
┌──────────┐              ┌──────────┐                    │
│          │              │ Commit 2 │                    │
│  More    │─────add─────▶│ "Fixed   │─────push───────────┘
│  edits   │              │  bug"    │
│          │              │          │
└──────────┘              └──────────┘
                                │
                          (Can go back
                           to any point)
```

## Emergency Commands

### Oops, I committed the wrong thing
```bash
# Undo last commit, keep changes
git reset --soft HEAD~1

# Undo last commit, discard changes
git reset --hard HEAD~1
```

### I want to see what I changed before committing
```bash
git diff
```

### I messed up, go back to last working version
```bash
git checkout .
# Warning: This discards ALL uncommitted changes
```

## GitHub Pages Specific

After you push to GitHub:

1. Go to repository Settings
2. Click "Pages"
3. Select `main` branch
4. Save
5. Wait 2-5 minutes
6. Visit `https://username.github.io/repository-name`

Every time you push, GitHub Pages updates automatically (takes ~1 minute).

## Tips for Designers

1. **Commit often** - Better to have many small saves than one giant one
2. **Write clear messages** - Your future self will thank you
3. **Don't commit huge files** - Keep images under 1MB when possible
4. **Pull before push** - If working with others, always pull first
5. **Branches are free** - Experiment without fear

## Resources

- [GitHub Desktop](https://desktop.github.com/) - GUI instead of command line
- [Git Visualization](https://git-school.github.io/visualizing-git/) - See Git in action
- [GitHub Pages Guide](https://pages.github.com/) - Official documentation

## Remember

- Git never loses committed work
- You can always go back
- When in doubt, commit before trying something new
- GitHub is just Git in the cloud

---

Happy versioning! 🎨✨
