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
- Make every entry useful to another agent who was not in the conversation.
  Include the local date/time, area, goal, work performed, concrete files or
  components affected, result/decision, verification performed, limitations,
  and the next specific step or blocker.
- Use the existing **Area**, **Worked on**, **Result**, and **Next step** labels
  so the public dashboard can render the entry. Put the goal, technical detail,
  verification, decisions, and limitations into those fields in complete
  sentences; do not rely on vague statements such as "worked on UI".
- Keep entries factual and detailed enough to summarize accurately. Do not
  record passwords, tokens, or other private credentials.
- Do not claim that a physical test, GitHub push, or software change happened
  unless it actually happened.
- Preserve verified historical entries, and do not reassign disputed work to
  Dad or Josiah without evidence.
- Keep each activity entry consistent with its matching session row. Every
  record change must regenerate and synchronize the public dashboard and push
  the appropriate private/public `main` branch(es); the update is incomplete
  until the canonical public dashboard reflects it.

## Activity

### 2026-10-16 — Josiah

- **Area:** Node-editor workflow, camera workspace, and machine activity data
- **Worked on:** Goal: make the browser editor easier to return to after
  capture work and reduce the need to rebuild workflows. Added a browser-local
  named graph library with Save, Save as, New, Open, and Delete; added
  Ctrl/Cmd+S to save, Ctrl/Cmd+D to duplicate the selected node, Home to fit
  the graph, Escape to return from gallery/live-preview overlays, smoother
  node/port/wire feedback, and a dismissible capture notice positioned above
  the bottom bar. Updated `index.html`, `studio.js`, and `studio.css`.
- **Result:** Added a local Pi-side `machine-activity.json` ledger and
  `/api/machine-metrics` endpoint in `server.py`. The UI now displays
  successful saved-photo totals plus puffer and light on/off transition totals.
  A count changes only after the existing camera/Pico request reports success;
  it is an operator activity record, not a safety interlock or hardware audit.
- **Next step:** Deploy all four UI/server files to the Pi together, restart
  the universal-nodes service, then verify one saved photo, one puffer cycle,
  and one light cycle update the bottom activity strip. Verification so far:
  Python syntax compilation, all 27 Python tests, and whitespace validation
  passed; browser/node tests could not run on this computer because Node.js is
  not installed.

- **Area:** Shared project records
- **Worked on:** Explicitly identified the active Book Scanner conversation as
  Josiah's and corrected the current session to include the earlier editor and
  workflow-improvement request from 15:08 CDT.
- **Result:** The stale Dad session was closed under the one-hour inactivity
  rule; the current Josiah session is checkpointed from its first observed
  project message and future work remains attributed to Josiah.
- **Next step:** Continue recording meaningful Book Scanner work as it is
  discussed or completed.

- **Area:** Session tracking preference
- **Worked on:** Chose uninterrupted background tracking for Josiah's active
  project session.
- **Result:** The session automation no longer asks inactivity questions or
  closes a session after silence; it checkpoints and publishes the active
  duration until Josiah explicitly stops it.
- **Next step:** Use the public dashboard to review the continuously updated
  project-time record.

### 2026-10-16 — Dad

- **Area:** Time-record identity correction
- **Worked on:** Explicitly clarified that Josiah, not Dad, was working at
  00:24, that 00:24 was Josiah's stop time, and that Dad logged in at 10:16.
- **Result:** Removed the incorrect overnight Dad attribution. Josiah's session
  is closed at 00:24 and split at midnight for correct daily totals. Under the
  selected silence rule, Dad's earlier session ran from 10:16:37 to 10:18:20,
  and Dad's correction message started a new session at 11:18:20. Dad then
  accepted both GitHub invitations, restoring public-dashboard write access;
  the session was checkpointed at 11:33:49.
- **Next step:** Keep checkpointing Dad's current session from observable
  project-message timestamps and synchronize the private tracking documents.

### 2026-10-15 — Josiah

- **Area:** Dashboard sharing
- **Worked on:** Set the public GitHub Pages address as the canonical Book
  Scanner dashboard link for both Josiah and Dad.
- **Result:** Future dashboard requests now use the no-login public address,
  rather than a private file link that can show a 404 page.
- **Next step:** Keep the public dashboard synchronized whenever a session or
  activity record changes.

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
