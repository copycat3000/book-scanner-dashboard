# Book Scanner Session Time Log

Shared project-conversation time log for Josiah and Dad. This records elapsed
conversation sessions, not unattended work or time spent away from the
keyboard.

## Recording rules

- A Book Scanner project message from an explicitly identified `Dad` or
  `Josiah` starts, resumes, or checkpoints that person's session at the
  message timestamp.
- Identity must be explicit. Never infer whether a message belongs to Dad or
  Josiah from a computer name, operating-system account, ChatGPT account,
  GitHub account, device, browser profile, or prior session. The `Computer`
  column is provenance only and does not establish session ownership.
- Preserve message timestamps at the finest precision actually available,
  including seconds and local timezone when the source exposes them. Never
  invent sub-minute precision. `Minutes` is calculated from the recorded
  timestamps and may be fractional; do not manually round away available
  precision.
- An explicitly started session continues as a user-approved background timer
  until that person explicitly asks to stop it. Do not send inactivity warnings
  and do not close a session merely because of silence.
- The configured session automation checkpoints open rows at its heartbeat
  timestamps. This background tracking policy was explicitly requested by
  Josiah on 2026-10-16.
- Preserve all verified historical rows. Do not reassign a disputed historical
  session to Dad or Josiah without evidence.
- Every record change must regenerate the dashboard from the Markdown sources,
  synchronize the matching private-repository copies, export the public-only
  files, commit the source records and generated dashboard together, and push
  the appropriate `main` branch(es). A record update is incomplete until the
  canonical public dashboard reflects it.
- Never put passwords, access tokens, or other secrets in this file.

## Activity tracking rules

- Keep a concise running summary of the Book Scanner work discussed or completed during each session.
- Update the activity summary whenever meaningful project work changes, and finalize it when the session ends.
- Record both work completed and significant work investigated/tested, distinguishing the two when useful.
- Make the summaries specific enough that either person can ask what Dad or Josiah worked on or accomplished on a given day.
- Do not infer unattended work; only record project activity evidenced by the conversation or repository changes.
- When Dad or Josiah asks about today's time/work or asks for the dashboard,
  return the canonical public dashboard link first, then answer from the
  current dashboard/source data for the requested local date.

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
| 2026-10-15 | Josiah | Copycat | 23:36 CDT | 00:00 CDT | 24 | Continued the shared GitHub time-and-activity dashboard work until midnight |
| 2026-10-16 | Josiah | Copycat | 00:00 CDT | 00:24 CDT | 24 | Finished the midnight portion of the dashboard/tracking session; Dad explicitly identified 00:24 as Josiah's stop time |
| 2026-10-16 | Dad | Codex desktop | 10:16:37 CDT | 10:18:20 CDT | 1.7167 | Explicitly identified himself as Dad; closed at exactly one hour before the next message after 1:01:43 of silence |
| 2026-10-16 | Dad | Codex desktop | 11:18:20 CDT | 12:33:49 CDT | 75.4833 | Corrected the midnight identity/session boundary and restored repository write access; auto-closed after one hour without a further project message |
| 2026-10-16 | Josiah | Copycat | 15:08:32 CDT | ongoing | 155.6333 | Started editor/workflow improvements; excludes 30 minutes spent on something else and was background-checkpointed at 18:14:10 CDT |

No Dad session or activity entry has been recorded for 2026-10-15. Dad
explicitly corrected the identity boundary on 2026-10-16: the 00:24 message
was Josiah's stop, and Dad logged in at 10:16 that morning. Because Dad's next
message arrived 1:01:43 later, the 10:16:37 session closes at 10:18:20 and a
new session starts at 11:18:20 under the selected 60-minute rule. That Dad
session was later closed at its one-hour checkpoint after no further project
message. Josiah later explicitly identified himself; his current session was
corrected to the first observed Book Scanner message at 15:08:32 CDT and
manually adjusted at 16:38:01 CDT to exclude 30 minutes spent on something else, then background-checkpointed at 17:09:02 CDT and 18:14:10 CDT. Josiah subsequently requested that active
sessions continue as background timers without inactivity prompts or closure.

## Query convention

When asked how much time a person spent on the project, return the canonical
public dashboard link first, read the current synchronized sources, and sum
`Minutes` for that person's local date. The active-session row is updated by
the configured, user-approved background timer.

## Important limitation

Active sessions are background-timed only while the configured session
automation is running. Each computer must have authenticated GitHub access if
it is expected to commit and push rows. Shared read access lets both people
inspect the log; it does not grant either computer permission to write.
