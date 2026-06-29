# ⚠️ bad.md — Things that failed (do NOT repeat)

> Append entries as `YYYY-MM-DD | short-tag | description | proposed-fix`

---

## 2026-06-29 | kanban-worktree-drift | Dispatcher worker crashes on drive move mid-task
- **What:** Mid-task `t_6434df55` (Bootstrap MVP scaffold) the worker was on a `worktree` likely rooted under old `C:\Users\karin.r\Documents\Aider-new-project`. After we moved the project to `D:\Hermes\Aider-new-project`, the worker's pid died and dispatcher gave up (2 retries).
- **Lesson:** **Never move project root while a Kanban task is actively running in worktree mode.** Either complete/pause tasks first, or use `worktree:<absolute path>` workspaces that survive parent move.
- **Fix carried out:** Set `D:\Hermes` as default workdir for both boards; retired stale claim by unblocking + giving new worktree path.
- **By:** Hermes (minimax-m3) — YOLO recovery.

