# Product Requirements Document (PRD) - TODO App Upgrade: Due Dates, Priorities, and Filters

## 1. Overview

The current TODO app is intentionally basic and currently supports only a task title and completion state. This PRD defines a simple, teachable upgrade that improves day-to-day task organization without adding backend complexity.

The MVP focuses on adding due dates, priorities, and quick date-based filters while keeping storage local. More advanced visual and ordering behavior is deferred to Post-MVP to keep initial implementation lean.

---

## 2. MVP Scope

- Add an optional `dueDate` field to each task.
- `dueDate` format must be ISO `YYYY-MM-DD`.
- Invalid `dueDate` values should be ignored and treated as absent.
- Add a `priority` field with enum values `P1 | P2 | P3`.
- Default `priority` to `P3` when no value is provided.
- Keep `title` required.
- Add filters/tabs for:
  - All
  - Today
  - Overdue
- Filter behavior:
  - All: show complete and incomplete tasks
  - Today: show incomplete tasks only
  - Overdue: show incomplete tasks only
- Keep storage local only.
- No backend or external storage changes.

---

## 3. Post-MVP Scope

- Visually highlight overdue tasks so they stand out.
- Add sorting with this priority:
  1. Overdue tasks first
  2. Then by priority (`P1` before `P2` before `P3`)
  3. Then by due date ascending
  4. Tasks without due dates last
- Add visual refinement for priority display (for example, color-coded priority badges).

---

## 4. Out of Scope

- Notifications
- Recurring tasks
- Multi-user support
- Keyboard navigation enhancements
- Special accessibility features beyond current baseline
- Any backend persistence changes
- External storage integrations
