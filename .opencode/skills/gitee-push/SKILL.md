---
name: gitee-push
description: Use when the user asks to commit and push the current project to Gitee. Commits all changes and pushes to https://gitee.com/wang-xiuning/wangxiuning2026 via SSH.
---

# Gitee Push

Commit all staged changes and push to the Gitee repository.

## Remote Repository

- URL: `https://gitee.com/wang-xiuning/wangxiuning2026`
- SSH: `git@gitee.com:wang-xiuning/wangxiuning2026.git`

## Steps

1. Check current status: `git status -u`
2. If remote `origin` is not set or points elsewhere, update it:
   - Check: `git remote -v`
   - If missing: `git remote add origin git@gitee.com:wang-xiuning/wangxiuning2026.git`
   - If wrong: `git remote set-url origin git@gitee.com:wang-xiuning/wangxiuning2026.git`
3. Stage all changes: `git add -A`
4. Commit with a descriptive message summarizing the changes: `git commit -m "<message>"`
5. Push to Gitee: `git push -u origin main` (or `master` depending on the repo's default branch)
6. If the push is rejected (non-fast-forward), pull first: `git pull --rebase origin main` then retry push.

## Notes

- Use SSH for authentication (key already configured at `~/.ssh/id_ed25519`).
- Determine the default branch name with `git branch --show-current` or `git remote show origin` before pushing.
- If the remote repository is empty, the first push must use `-u` to set upstream tracking.
