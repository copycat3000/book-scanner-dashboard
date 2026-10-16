# Book Scanner — Public Project Dashboard

This public site contains only the Book Scanner project-time dashboard and the
two Markdown records that supply its data:

- `index.html` — downloadable, offline dashboard
- `SESSION_TIME_LOG.md` — recorded conversation sessions and time
- `PROJECT_ACTIVITY_LOG.md` — recorded daily project work

The Book Scanner software, hardware documents, engineering handoff, and any
credentials remain in the separate private engineering repository.

Canonical public dashboard:
https://copycat3000.github.io/book-scanner-dashboard/

## Synchronization contract

- `SESSION_TIME_LOG.md` and `PROJECT_ACTIVITY_LOG.md` are the public data
  authority. The generated `index.html` contains only data parsed from those
  sources.
- The matching private-repository records, project guide, engineering handoff,
  dashboard generator, and public export workflow must all implement the same
  message-driven session policy documented in the time log.
- Any change to either record must regenerate the dashboard, synchronize the
  private and public copies, commit the source records and generated output
  together, and push the appropriate `main` branch(es). The update is not
  complete until the public URL reflects it.
- When Dad or Josiah asks about today's time/work or asks for the dashboard,
  return the canonical public URL first and answer from the current
  dashboard/source data.
- The public export remains limited to this README, the two Markdown logs, and
  the generated dashboard. Private engineering documents, credentials, and
  scanner application code must not be published here.
