# fremo

> Codename. Will probably change.

An AI-native CRM where a deal is a conversation, not a form.

## The goal

Every CRM ever built asks a salesperson to stop selling and go update a record.
Stages, fields, dropdowns, required-before-you-can-save. The work happens in
email, calls, and WhatsApp; the CRM is the tax you pay afterwards. So the data
is always late, always thin, and the reports built on top of it are guesses
wearing a suit.

fremo inverts it. Each deal is a thread. You talk to an agent in that thread the
same way you'd talk to a colleague who has been on every call with you:

- *"Ana wants net-60, said she'd loop in legal"*
- *"why has Acme gone quiet?"*
- *"what's actually closing this month?"*

The agent keeps the record. You keep selling.

## Manifesto

**1. The log is the truth.**
A deal is an append-only stream of what happened: emails, calls, notes,
meetings, decisions, your own messages. Nothing is overwritten. Nothing is lost
to someone re-typing a stage. History is the product.

**2. Structure is derived, not demanded.**
Stage, value, next step, risk — the agent infers them from the log. You can
override any of them, and the override is itself an event, so the record shows
that a human disagreed and when. You never fill a form to make the software
happy.

**3. Chat is the interface, not a bolt-on copilot.**
Not a CRM with an AI sidebar. The thread *is* the deal. Reading, updating,
asking, reporting — all of it happens by talking.

**4. Numbers are arithmetic, not vibes.**
The agent narrates, but a forecast is computed over real state. An LLM
freestyling a pipeline total is a liability, not a feature.

**5. The agent proposes, the human disposes.**
Anything that leaves the building — an email, a commitment, a price — is
reviewed by a person. Internal bookkeeping can be autonomous. Those are
different risk classes and get treated differently.

**6. Your data is yours.**
Open source. Self-hostable. Plain, exportable, boring storage. A CRM that holds
your customer relationships hostage has already failed you.

**7. Small enough to understand.**
Deals, threads, events, an agent. If a feature needs a new noun, it needs to
earn it. Most CRMs are 200 features holding 6 hostage.

## Status

Thinking out loud. No code yet, on purpose.

Design notes live in [`docs/`](docs/).
