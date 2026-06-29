# 🗂️ kanban/ — Multi-agent handoff logs

This folder is the **on-disk mirror** of the Hermes Kanban board.  
Each file represents a **card** moving through columns:

`todo → in_progress → review → done → archive`

### File naming
`YYYY-MM-DD__<agent>__<short-tag>.md`  
e.g. `2026-06-29__ceo__define-blueprint.md`

### Card template
```markdown
# <Title>

**Column:** todo | in_progress | review | done
**Owner:** <agent or human>
**Created:** YYYY-MM-DD
**Updated:** YYYY-MM-DD

## Goal
<one-liner>

## Acceptance
- [ ] …

## Hand-off log
- 2026-06-29 13:15 | ceo → researcher | <note>
```

## Current board (mirror)
<!-- updated by Hermes on each hand-off -->

| Card | Owner | Status | Updated |
|---|---|---|---|
| (empty) | — | — | — |

