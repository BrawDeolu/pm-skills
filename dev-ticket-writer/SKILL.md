---
name: dev-ticket-writer
description: Turn a PRD, FRD, feature idea or prototype into engineering tickets split into UI and API tickets, written in plain English with Why, Scope, Not included, Given/When/Then acceptance criteria and Tech notes. Use for backlog grooming, sprint prep, or rewriting messy tickets.
---

# Dev Ticket Writer

Write tickets that a frontend or backend engineer can pick up and finish without asking the PM what was meant. Tickets are split by **who builds them** (UI and API), not by product area, because that is how engineers pull work.

## Step 1. Gather the source

Use whatever exists: PRD or FRD, a prototype link or file, screenshots, a Slack thread, or a plain description. If there is a working prototype, walk through it screen by screen first. Every screen and every state in the prototype should map to at least one UI ticket.

Ask only if something blocks you, for example: "Is there already an endpoint for X, or do we need a new one?"

## Step 2. Split the work

- **[API] tickets**: endpoints, data models, background jobs, sending, billing, webhooks, permissions checks, tracking events stored server side.
- **[UI] tickets**: screens, components, states (empty, loading, error, success), copy, client-side validation, analytics events fired from the client.
- **[Config] tickets** (only if needed): feature flags, plan limits, templates, settings someone changes without code.

Order tickets so dependencies are obvious, and say which tickets must ship together, for example: "API 1 to 3 and UI 2 ship together, or the link in the email will not work."

## Step 3. Ticket format

Title format: `[UI] Verb + object` or `[API] Verb + object`. Number them within the epic (API 1, API 2, UI 1...).

```
### API 1. [API] Create unsubscribe links and add the footer when emails are sent

**Why**
One or two sentences. The user or business reason, not the technical one.

**Scope**
- What is being built, one bullet per behaviour.
- Specific copy in quotes where the user will see it.

**Not included**
- What someone might assume is in this ticket but is not.

**Acceptance criteria**
- **Given** <starting state>, **when** <action>, **then** <result>.
- Cover the happy path, empty state, error state, limits and repeat actions
  (clicking twice, link opened twice).

**Tech notes**
- Pointers for engineering: relevant endpoints or tables, standards or RFCs,
  similar code paths that already work, gotchas, performance limits.

**Priority:** P0 / P1 / P2
```

Extras when relevant:
- **Tracking**: a small table of Event | When | Properties inside the ticket that builds it, so data is built in, not bolted on later.
- **Screenshot or prototype link** for every UI ticket, full screen rather than cropped, so the engineer sees context.

## Step 4. Writing rules

- **Plain English.** Write so a new engineer, a QA tester and a support lead can all read it. No jargon that is not needed. If a technical term is needed, put it in Tech notes, not in Scope.
- One ticket is something one person can finish in a sprint. If it is bigger, split it.
- Never assume data names. If users name their own fields or events in the product, the ticket must work for any name.
- Do not invent endpoints or tables as fact. Write "likely" or "check if" when you are guessing.
- No ticket without acceptance criteria.
- Do not push tickets into a project management tool unless the person asks. Return them in the chat or doc by default.

## Step 5. Close with

1. A summary line: "API tickets: 6. UI tickets: 6." plus what ships together.
2. **Open items**: questions that need a decision (legal wording, permissions, migration).
3. One next step (FRD, prototype, or create the tickets in their tool if they want).

## Check before sending

- Every ticket title starts with [UI], [API] or [Config].
- Every ticket has Why, Scope, Not included, Acceptance criteria, Tech notes, Priority.
- Every prototype screen and state is covered by a UI ticket.
- No ticket depends on a field name the product does not guarantee.
