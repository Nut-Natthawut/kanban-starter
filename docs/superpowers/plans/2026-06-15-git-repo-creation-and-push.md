# Git Repository Creation and Push Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rename the existing git origin remote to upstream, create a new public remote repository on GitHub named kanban-starter under the user account Nut-Natthawut, and push the local codebase.

**Architecture:** We use git commands and the GitHub CLI (gh) to create the remote repository, configure the remotes, and push the repository branches.

**Tech Stack:** Git, GitHub CLI (gh)

---

### Task 1: Rename Remote and Create GitHub Repo

**Files:**
- Modify: git configuration (remotes)

- [ ] **Step 1: Rename existing origin remote to upstream**

Run: `git remote rename origin upstream`
Expected: Success with no output.

- [ ] **Step 2: Verify the remote was renamed**

Run: `git remote -v`
Expected:
```
upstream	https://github.com/kittipitch/kanban-starter.git (fetch)
upstream	https://github.com/kittipitch/kanban-starter.git (push)
```

- [ ] **Step 3: Create GitHub repository and push current repository**

Run: `gh repo create kanban-starter --public --source=. --remote=origin --push`
Expected: Output showing the repository `Nut-Natthawut/kanban-starter` was created and the current branch pushed to it.

- [ ] **Step 4: Verify the new remote origin is configured**

Run: `git remote -v`
Expected:
```
origin	https://github.com/Nut-Natthawut/kanban-starter.git (fetch)
origin	https://github.com/Nut-Natthawut/kanban-starter.git (push)
upstream	https://github.com/kittipitch/kanban-starter.git (fetch)
upstream	https://github.com/kittipitch/kanban-starter.git (push)
```

- [ ] **Step 5: Verify GitHub repo info**

Run: `gh repo view Nut-Natthawut/kanban-starter`
Expected: Output showing details of the new public repository.
