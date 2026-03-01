---
name: git-push
description: Upload local code changes to remote Git repository. Use this skill whenever the user wants to push, upload, or sync local code to remote, or says things like "上传代码", "push 代码", "提交到远端", "同步到 git".
---

# Push Code to Remote

## Steps

1. **Get current branch name**
```bash
   git branch --show-current
```

2. **Pull latest changes first**
```bash
   git pull origin <current-branch>
```
   If conflicts arise, stop and ask the user to resolve them before continuing.

3. **Review the diff to understand changes**
```bash
   git diff origin/<current-branch>
```

4. **Stage all changes**
```bash
   git add .
```
   Skip files that should not be committed (e.g. `.env`, build artifacts, `bin/`, `obj/`).

5. **Commit with an auto-generated message** based on the diff
   - Follow Conventional Commits: `type(scope): description`
   - Types: `feat` / `fix` / `refactor` / `chore` / `docs`
   - Description in English, explain **what** changed, not **how**
   - Don't include any ai assistant as co-author in the commit message.
```bash
   git commit -m "feat(order): add idempotency check for purchase order handler"
```

6. **Push to remote**
```bash
   git push origin <current-branch>
```