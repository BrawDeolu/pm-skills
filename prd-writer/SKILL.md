---
name: prd-writer
description: Write or review a PRD or FRD (feature requirements document). Use when someone asks for a PRD, FRD, spec, requirements doc, user stories with acceptance criteria, or wants a PRD critiqued before engineering picks it up.
---

# PRD Writer

Write product requirement documents that engineers, designers and QA can build and test from without a follow-up meeting. Also review existing PRDs and point out what will break once engineering reads them.

Two modes:
- **Write mode**: a new PRD (whole product) or FRD (one feature or module).
- **Review mode**: someone shares a PRD and asks what is wrong with it.

---

## Write mode

### Step 1. Get the inputs (ask only for what is missing)

1. **Product or feature name** and one sentence on what it does.
2. **Primary user**: role, context, what they do today instead.
3. **The problem** in the user's words, plus any evidence (support tickets, usage data, sales calls).
4. **Goal and success metric**: what number moves, by how much, by when.
5. **Constraints**: deadline, team size, tech limits, regulation, budget.
6. **Template**: if the person or their company has a house PRD template, use it exactly. Their template always beats this one.

If the request is clear, start writing and list your assumptions at the top for them to confirm. Do not hold the whole document back for questions. If no name is given, pick a working title and say it is a working title.

### Step 2. Use this structure (unless they gave a template)

**PRD (whole product)**
1. Title, version, date, status (Draft, In review, Approved)
2. Team and sign-off table: Role | Name | Sign-off date. Usually PM, Design, Frontend, Backend, QA, Head of Product.
3. Overview: 2 to 4 sentences. What it is and who it is for.
4. Problem statement: who hurts, how, how often, what it costs them. Evidence if any.
5. Objectives: 3 to 5, each tied to a metric.
6. Personas: 1 to 3, short. Role, context, current workaround, what "done well" looks like for them.
7. Constraints: grouped as Technical, Resourcing and timeline, Market and legal.
8. Risks and measures: table of Risk | Likelihood | Impact | Mitigation.
9. Use cases: short list of the jobs the product must do.
10. Features: one module per feature (format below).
11. Success metrics: split into **leading** (early signals, weeks) and **lagging** (outcomes, months). Say how each is measured.
12. Out of scope: an explicit list. This section prevents more arguments than any other.
13. Open questions: things that need a decision, with an owner if known.

**FRD (one feature)**: Title and sign-off, Overview, Problem statement, the feature module, Success metrics and tracking events, Out of scope, Open questions.

### Step 3. Write each feature module like this

**Module introduction**: one short paragraph. What the feature does and why it exists.

**Functional requirement overview**

| Req No | Requirement | Description |
|---|---|---|
| FR-1 | Create a segment | User can build a segment from filters on attributes and events |

**User stories and acceptance criteria**

| Req No | Requirement | User story | Acceptance criteria |
|---|---|---|---|
| FR-1 | Create a segment | As a marketer, I want to... so that... | Gherkin scenarios (below) |

Acceptance criteria use Gherkin (Given / When / Then / And). One scenario per behaviour, and always cover:
- the happy path
- empty states (no data yet)
- validation errors (bad input, limits reached)
- permission or plan limits
- failure (network down, third party down)

```
Scenario: User reaches the keyword limit on their plan
  Given the user is on a plan that allows 5 keywords
  And they already have 5 keywords
  When they try to add another keyword
  Then the Add button is disabled
  And they see "You've used all 5 keywords on your plan. Upgrade to add more."
```

**Priority**: label each requirement P0 / P1 / P2 or MoSCoW. Explain any surprising priority call in one line.

**Tracking events** (where the feature needs measuring): table of Event | When it fires | Properties. Build the data in now, not later.

**User flow** and **UI/UX design**: leave link placeholders if designs do not exist yet.

### Step 4. Writing rules
- Plain English. Short sentences. If a non-technical stakeholder would stumble on a word, replace it.
- No filler ("seamless", "robust", "leverage", "best-in-class").
- Every requirement must be testable. If QA cannot write a test from it, rewrite it.
- Use real numbers from the person. **Never invent statistics, market sizes or research findings.** If a number is needed and you do not have it, write `[TBC: source needed]`.
- Do not assume field names, data formats or integrations exist. If users can name things freely in the product, requirements must not depend on specific names.
- List every product decision you made on their behalf in a short "Decisions to confirm" section at the end.

### Step 5. Deliver
Deliver in the format the person works in (a doc, Word file, Notion page, markdown). End with the "Decisions to confirm" list and one next step (tickets, prototype or review).

---

## Review mode

Read the whole document, then report problems most damaging first:

1. **Viability**: unit economics that cannot work, legal or licensing gaps, scope that is not really an MVP, users who would not actually do this.
2. **Contradictions an engineer will hit**: two sections that disagree (fees, states, timing, permissions). Cite the section numbers.
3. **Gaps**: no problem statement, no metrics, no edge cases, no failure states, no offline or low-bandwidth path where users need one, no out-of-scope list.
4. **Testability**: requirements QA cannot test.
5. **Document hygiene**: numbering, naming drift, undefined terms.

For each issue give what it is, where it is, why it matters and a fix in one or two lines. Close by offering to rewrite the worst section or turn a messy rule into a decision table.

Be direct. A PRD review that only praises is useless.
