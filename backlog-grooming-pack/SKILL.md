---
name: backlog-grooming-pack
description: Groom one or more backlog items end to end into a single shareable "sprint pack": an FRD, data insights and success metrics, a clickable prototype and UI/API tickets per item. Use when a PM wants backlog items ready for sprint planning or stakeholder review in one place.
---

# Backlog Grooming Pack

Take raw backlog items ("let users send a test campaign", "add email unsubscribe") and make each one sprint-ready. The output is one file or page with a tab per backlog item, and inside each item four views:

1. **FRD**
2. **Data insights**
3. **Prototype**
4. **Tickets**

This skill works well alongside `prd-writer` (for the FRD format) and `dev-ticket-writer` (for the ticket format). If those are installed, follow them for those parts.

## Step 1. Collect the inputs

For each backlog item get:
- The one-line request and who asked for it (customer, sales, support, internal).
- Any evidence: customer quotes, support volume, usage numbers. **Use only real numbers from the person or their data. Never invent figures.**
- The current product: a screenshot, a live link, or an HTML clone of the app. A clone of the real UI makes the best prototypes.
- Known constraints: pricing, plan limits, regulation, what the product does not support.

Before designing, check assumptions about the product's data. Common trap: assuming standard field or event names when every customer names their own. If you are unsure, ask.

## Step 2. For each item, build the four views

### FRD
Overview, Problem statement, the feature module (requirement table plus user stories with Given/When/Then acceptance criteria), Out of scope, Open questions. Keep assumptions out of the final version unless the person asks for them; raise them as questions instead.

### Data insights
- **What the data should tell us**: the questions this feature should answer after launch.
- **Customer insights to gather**: what to ask customers before and after release.
- **Success metrics**: leading and lagging, with a target if the person has one.
- **Tracking events**: Event | When it fires | Properties.

A useful grouping for metrics: Growth (adoption, new users of the feature), Usage (frequency, depth), Data health (completeness, errors), Quality (success rate, support tickets), and AI quality if the feature uses AI (accuracy, fallback rate, user overrides).

### Prototype
- Build on top of the real product UI where possible so it looks and behaves like the product. Add the new feature as a layer rather than redesigning screens.
- Cover every state: empty, loading, success, error, limit reached, permission denied.
- List the screens (for example "Test send: choose recipients", "Test send: insufficient balance") and let each one open the prototype on that screen.
- Test every flow in a browser before delivering. Fix layout overlaps and dead clicks.

### Tickets
UI and API tickets with Why, Scope, Not included, Acceptance criteria, Tech notes and Priority. Add a full-screen screenshot of the relevant prototype screen to each UI ticket. Add a filter for UI, API and Config.

## Step 3. Assemble the pack

One self-contained HTML page (or a doc with tabs if the person prefers):
- Left side: list of backlog items with ticket count and priority.
- Header per item: name, user story, epic, priority, ticket summary.
- Tabs: FRD, Data insights, Prototype, Tickets.
- Works offline as a single file and at phone width.

Optional extras when asked: standalone PDF of each FRD, a zip of tickets with screenshots organised by ticket.

## Step 4. Check and hand over

- Open every tab and every prototype screen. No empty tabs.
- Tickets match the prototype; the prototype matches the FRD.
- List what is new and not yet reviewed by the person, and anything you designed without seeing the real screen, so they know where to look first.
