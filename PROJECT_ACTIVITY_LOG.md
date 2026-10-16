# Book Scanner Project Activity Log

Shared daily activity record for Josiah and Dad. This records project work and
conversation tasks; it is not a substitute for the source-code history or the
time log.

## Recording rules

- A Book Scanner project message from an explicitly identified `Dad` or
  `Josiah` starts, resumes, or checkpoints that person's activity at the
  message timestamp. Add or update an entry when the message provides evidence
  of meaningful project work.
- Use only the explicitly supplied display name: `Josiah` or `Dad`. Never
  infer identity from a computer, operating-system account, ChatGPT account,
  GitHub account, device, browser profile, or prior session.
- Include the local date, approximate time, area worked on, work performed,
  result, and next step or blocker.
- Keep entries factual and concise. Do not record passwords, tokens, or other
  private credentials.
- Do not claim that a physical test, GitHub push, or software change happened
  unless it actually happened.
- Preserve verified historical entries, and do not reassign disputed work to
  Dad or Josiah without evidence.
- Keep each activity entry consistent with its matching session row. Every
  record change must regenerate and synchronize the public dashboard and push
  the appropriate private/public `main` branch(es); the update is incomplete
  until the canonical public dashboard reflects it.

## Activity

### 2026-10-16 — Dad

- **Area:** Time and activity tracking
- **Worked on:** Directed the Book Scanner records to use precise observable
  message timestamps, explicit Dad/Josiah identity, the 60-minute silence
  boundary, and mandatory public-dashboard synchronization; then explicitly
  identified himself as Dad for this conversation.
- **Result:** Dad's earlier same-conversation messages can now be attributed
  without relying on a computer or account label. Under the selected rule, the
  00:24:07 session closed at 09:16:37, exactly one hour before the 10:16:37
  message, and a new session began at 10:16:37.
- **Next step:** Keep checkpointing Dad's current session from observable
  project-message timestamps and publish the prepared private/public record
  changes when repository write access is available.

### 2026-10-15 — Josiah

- **Area:** Public project dashboard
- **Worked on:** Approved a no-login publishing route for the shared time and
  activity dashboard while retaining the scanner software and engineering
  repository as private.
- **Result:** Created the public dashboard-only publication workflow. It
  exports exactly the dashboard, session log, activity log, and public README.
- **Next step:** Keep the public export synchronized after each recorded
  time/activity update and use the GitHub Pages link to view it without login.

- **Area:** Dashboard data integrity
- **Worked on:** Made the dashboard's contributor list and all project-time
  and activity content explicitly Markdown-sourced.
- **Result:** The generated HTML now identifies the two Markdown logs as its
  only data authority and never uses a project database, API, or hand-edited
  dashboard values.
- **Next step:** Update the two Markdown logs whenever project work or session
  time changes; regenerate and push the dashboard alongside them.

- **Area:** Shared project reporting
- **Worked on:** Started a professional offline HTML dashboard that turns the
  shared session and activity Markdown logs into daily time analytics,
  contributor totals, a session ledger, and a searchable work history.
- **Result:** The dashboard will be rebuilt and pushed with every recorded
  session-time update so Dad can download the current report from GitHub.
- **Next step:** Review the generated report from GitHub and keep the logs
  factual as work is completed.

- **Area:** Project coordination and shared records
- **Worked on:** Added shared time tracking and requested a shared activity
  history so Josiah and Dad can see what each person worked on.
- **Result:** Created and pushed `SESSION_TIME_LOG.md` and this activity log.
- **Next step:** Record future meaningful work here and query this file by
  person/date when asked.

- **Area:** Puffer and lighting control
- **Worked on:** Added the Book Scanner Lights node, deployed it to the Pi,
  assigned its current commissioning control to GP28, and preserved GP27 for
  the C035B puffer.
- **Result:** The Lights node includes on/off controls and configurable
  brightness/PWM control. The Run button was also fixed to start at the
  `When Start Pressed` node and follow connected event wires.
- **Next step:** Physically validate one LED section, PWM brightness levels,
  current, heat, and the lighting board's PWM behavior.

- **Area:** Graph timing and operator controls
- **Worked on:** Added start/stop controls for the Always-On Monitor's
  repeating timer and fixed the Start button so it wakes the graph runtime.
- **Result:** Changes were tested with the existing 25 Python tests and pushed
  to GitHub. Latest recorded commit: `0d61e18`.
- **Next step:** Refresh the Pi UI and test the monitor and lights on the
  physical setup.

## Query convention

When Dad or Josiah asks what someone worked on today or asks for the dashboard,
return the canonical public dashboard link first, then read the current
synchronized source data and list that person's entries for today's local
date. Distinguish completed work, work in progress, and blockers. Use Git
history to verify repository changes when useful.

## Important limitation

This is not a background activity tracker. ChatGPT can record work discussed or
performed during a conversation, but cannot know about offline work unless the
person reports it or a separate local automation records it.
