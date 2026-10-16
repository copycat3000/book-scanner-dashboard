# Book Scanner — Public Project Dashboard

This public site contains only the Book Scanner project-time dashboard and the
two Markdown records that supply its data:

- `index.html` — downloadable, offline dashboard
- `SESSION_TIME_LOG.md` — recorded conversation sessions and time
- `PROJECT_ACTIVITY_LOG.md` — recorded daily project work

The Book Scanner software, hardware documents, engineering handoff, and any
credentials remain in the separate private engineering repository.

Canonical public URL:
https://copycat3000.github.io/book-scanner-dashboard/

## Synchronization contract

- `SESSION_TIME_LOG.md` and `PROJECT_ACTIVITY_LOG.md` are the public data
  authority. The generated `index.html` must contain only data parsed from
  those sources.
- The matching private-repository records, `CHATGPT_PROJECT_GUIDE.md`,
  `AI_HANDOFF.md`, the dashboard generator, and the public export workflow must
  all implement the same message-driven session policy documented in the time
  log.
- Any change to either record must regenerate the dashboard, synchronize the
  private and public copies, commit the source records and generated output
  together, and push the appropriate `main` branch(es). Do not report the
  record update as complete until the public URL shows it.
- When Dad or Josiah asks about today's time/work or asks for the dashboard,
  return the canonical public URL first and answer from the current
  dashboard/source data.
- The public export must remain limited to this README, the two Markdown logs,
  and the generated dashboard. Do not publish private engineering documents,
  repository credentials, or scanner application code here.
