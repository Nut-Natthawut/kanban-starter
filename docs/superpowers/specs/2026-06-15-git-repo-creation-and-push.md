# Design Spec: Create New GitHub Repository and Push

## Overview
This document specifies the design and steps to create a new public GitHub repository under the user account `Nut-Natthawut` for the `kanban-starter` project and push the current codebase to it.

## Current State
- Local directory: `/Users/mac/Documents/Ai Spec/kanban-starter`
- Local Git repository: Initialized.
- Remote `origin` currently points to: `https://github.com/kittipitch/kanban-starter.git`

## Requirements
- Create a **public** GitHub repository named `kanban-starter` under user `Nut-Natthawut`.
- Push the local codebase to the new repository.
- Retain existing Git history.
- Retain a reference to the original starter repository by renaming the old `origin` to `upstream`.

## Proposed Design
1. **Rename Remote**: Rename the existing remote `origin` to `upstream`:
   ```bash
   git remote rename origin upstream
   ```
2. **Create Remote Repo & Push**: Create the new repository and push the local commits using the GitHub CLI:
   ```bash
   gh repo create kanban-starter --public --source=. --remote=origin --push
   ```

## Verification Plan
1. Check configured remotes:
   ```bash
   git remote -v
   ```
   Verify that `origin` points to `Nut-Natthawut/kanban-starter` and `upstream` points to `kittipitch/kanban-starter`.
2. Verify GitHub repository status:
   ```bash
   gh repo view Nut-Natthawut/kanban-starter
   ```
