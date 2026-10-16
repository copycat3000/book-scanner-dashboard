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
- If the next project message from that person is less than 60 minutes after
  the previous project message, checkpoint the same session at the new message
  timestamp.
- If the next project message from that person arrives after **60 minutes or
  more of silence**, close the previous session at exactly **one hour before
  the new message timestamp**, then start a new session at the new message
  timestamp. This implements Bruce's rule of subtracting the final unattended
  hour.
- Apply closure retroactively when the next message makes the silence gap
  observable. Do not claim background observation, a silently running timer,
  or an automatic stop that was not actually performed by separate automation.
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
| 2026-10-15 | Josiah | Copycat | 23:36 CDT | ongoing | 0 | Started a shared GitHub time-and-activity dashboard and mandatory push-on-record-update workflow |

No Dad session or activity entry has been recorded for 2026-10-15.

## Query convention

When asked how much time a person spent on the project, return the canonical
public dashboard link first, read the current synchronized sources, and sum
`Minutes` for that person's local date. A current message may checkpoint an
open row at its timestamp, but no interval may be presented as background
observation.

## Important limitation

This is message-driven accounting, not a background timer. A chat assistant can
only checkpoint or close a session when a later observable event supplies a
timestamp. Each computer must have authenticated GitHub access if it is
expected to commit and push rows. Shared read access lets both people inspect
the log; it does not grant either computer permission to write. No chat
assistant can reliably perform a silent GitHub push during an hour with no
messages unless separately configured local automation is actually running.
