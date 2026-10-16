# Book Scanner Session Time Log

Shared project-conversation time log for Josiah and Dad. This records elapsed
conversation sessions, not unattended work or time spent away from the
keyboard.

## Recording rules

- Add one row per active project-conversation session.
- Update the current row whenever a project session starts, stops, resumes, or
  reaches another one-hour checkpoint while messages are actively being sent.
- A session ends after a gap of more than one hour without a project message;
  finalize that row when the next project session starts or when the log is
  next accessed.
- `Minutes` is the elapsed session estimate, rounded to the nearest minute.
- Use the person's chosen display name consistently (`Josiah` or `Dad`).
- Record local timezone with the timestamps.
- Every time this record changes, regenerate `PROJECT_TIME_DASHBOARD.html` with
  `python3 tools/update_project_time_dashboard.py`, commit the record and
  dashboard together, and push them to `origin/main` when authenticated.
- Never put passwords, access tokens, or other secrets in this file.

## Activity tracking rules

- Keep a concise running summary of the Book Scanner work discussed or completed during each session.
- Update the activity summary whenever meaningful project work changes, and finalize it when the session ends.
- Record both work completed and significant work investigated/tested, distinguishing the two when useful.
- Make the summaries specific enough that either person can ask what Dad or Josiah worked on or accomplished on a given day.
- Do not infer unattended work; only record project activity evidenced by the conversation or repository changes.
- When asked what someone did today, read this file and summarize that person's activity entries for the requested date.

## Dashboard metadata

- **Dashboard contributors:** Josiah, Dad
- **Time-data source:** This file's `## Sessions` table.
- **Activity-data source:** `PROJECT_ACTIVITY_LOG.md`.

The dashboard must derive its project data only from these Markdown sources.
Do not add project time, people, sessions, or activity information directly to
the generated HTML.

## Sessions

| Date | Person | Computer | Start (local) | End (local) | Minutes | Work / activity summary |
|---|---|---|---|---|---:|---|
| 2026-10-15 | Josiah | Copycat | 15:45 CDT | 16:00 CDT | 15 | Initial active conversation session; UI and hardware-control work recorded below |
| 2026-10-15 | Josiah | Copycat | 17:55 CDT | 18:44 CDT | 45 | Resumed to repair shared-record querying; auto-closed after no response to the 45-minute check-in |
| 2026-10-15 | Josiah | Copycat | 23:36 CDT | ongoing | 0 | Started a shared GitHub time-and-activity dashboard and mandatory push-on-record-update workflow |

No Dad session or activity entry has been recorded for 2026-10-15.

## Query convention

When asked how much time a person spent on the project, read this file and sum
`Minutes` for that person's local date. An `ongoing` row may be estimated from
the current message timestamp, but must not be presented as exact background
tracking.

## Important limitation

This is not a background timer. ChatGPT must read this file before answering a
time question and update the current session at session start, session stop,
resume, and active one-hour checkpoints. Each computer must have its own
authenticated GitHub access if it is expected to commit and push rows. Shared
read access lets both people inspect the log; it does not grant either computer
permission to write. No chat assistant can reliably perform a silent GitHub
push after an hour with no messages unless a separately configured local
automation is running.
