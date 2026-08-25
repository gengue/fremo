# Docs

Design notes for fremo. Written before code, so the arguing happens in Markdown
where it's cheap.

Nothing here is final. Documents get replaced when a better idea shows up.

## Index

Nothing formal yet — see [Open questions](#open-questions) below.

## Decisions so far

### Substrate: event log + derived projections

A deal is an append-only event log. Structured state (stage, value, next step,
risk) is *derived* from that log by the agent and cached in a queryable shape.

```
events (append-only, source of truth)
   |
   v  projection
deal state (stage, value, next step, risk) -- derived, cached, queryable
   |
   v
agent reads state for aggregates, reads events for narrative
```

Rejected alternatives:

- **Classic CRM record + chat sidebar.** Fields as source of truth put the human
  back in the data-entry seat and reduce the agent to a copilot on the side.
- **Chat only, no structure at all.** "What closes this quarter?" would mean
  scanning every thread on every question: slow, expensive, non-deterministic.
  Forecasts need arithmetic over real state.

Human overrides are recorded as events too, so the log stays complete and the
agent can see where its inference was corrected.

## Open questions

- **Ingestion.** What fills the log in v1 — email sync, human notes typed into
  the thread, calendar, call transcripts? Without inbound events this is a notes
  app.
- **Agent autonomy.** Read-and-summarize only, or does it draft and send?
- **Who it's for.** Solo founder, small sales team, agency? Changes everything
  about multiplayer and permissions.
- **Multiplayer.** One thread, many humans, one agent — how does that read?
- **Stack.** Undecided. Deliberately last.
