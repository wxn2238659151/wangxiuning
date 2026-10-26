---
name: github-push
description: Use when the user asks to commit and push the current project to GitHub. Commits all changes and pushes to https://github.com/wxn2238659151/wangxiuning via SSH.
---

# GitHub Push

Commit all staged changes and push to the GitHub repository.

## Remote Repository

- HTTPS: `https://github.com/wxn2238659151/wangxiuning`
- SSH: `git@github.com:wxn2238659151/wangxiuning.git`

## Steps

1. Check current status: `git status -u`
2. If remote `github` is not set or points elsewhere, update it:
   - Check: `git remote -v`
   - If missing: `git remote add github git@github.com:wxn2238659151/wangxiuning.git`
   - If wrong: `git remote set-url github git@github.com:wxn2238659151/wangxiuning.git`
   - If `github` already exists alongside a `gitee` remote, keep both — do NOT replace `gitee`
3. Stage all changes: `git add -A`
4. Commit with a descriptive message summarizing the changes: `git commit -m "<message>"`
5. Determine the default branch: `git branch --show-current`
6. Push to GitHub: `git push github <branch>` (use `-u github <branch>` the first time)
7. If the push is rejected (non-fast-forward), pull first: `git pull --rebase github <branch>` then retry push.

## Notes

- Use SSH for authentication (public key is already configured by the user).
- The project may have **two** remotes: `gitee` (existing) and `github` (this skill's target). Do NOT overwrite `gitee`.
- If the remote repository is empty, the first push must use `-u` to set upstream tracking.
- This skill only handles `github` remote; if the user also wants Gitee pushed, use the `gitee-push` skill separately.
