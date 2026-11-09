---
name: annotated-product-guide
description: Write product guides, help articles and internal feature guides with annotated screenshots (arrows, numbered labels, boxes and redacted personal data). Use when someone asks for a product guide, user guide, help doc, how-to or wants screenshots annotated.
---

# Annotated Product Guide

Produce feature guides that show people exactly where to click. Each feature is a few short prose sections, each followed by a full-screen screenshot with clear annotations.

## Step 1. Set up the guide

Confirm:
- **Audience**: customers, support team, sales, new hires.
- **Format**: doc, PDF, help-centre article, or just the annotated images.
- **House style**: if the team already has a guide, match its structure, tone and annotation style exactly.

Default guide structure per feature:
1. **What it is**: one or two sentences.
2. **Who it is for and when to use it.**
3. **How to get there**: navigation path, with a screenshot.
4. **Step-by-step**: one numbered step per action, each with a screenshot if the screen changes.
5. **What each part of the screen means**: one annotated screenshot with numbered labels.
6. **Limits and plans**: what is restricted and on which plan.
7. **Common questions and troubleshooting.**

Write in plain English, second person ("Click Top Up"). Use the exact button labels from the product, in bold.

## Step 2. Annotate screenshots

Use full-screen screenshots so readers see where they are. Annotation style (keep it the same across the whole guide):

- **Arrows**: solid red (around #FF3B30), thick enough to see at reduced size, straight lines with a clear arrowhead. Avoid arrows crossing each other or crossing important UI.
- **Labels**: white boxes with a red border and dark text, placed next to the arrow's tail. Number them (1, 2, 3) only when the order matters or when the text refers to them by number.
- **Boxes**: rounded red rectangles to group an area (a table header, a set of fields).
- **Redaction**: grey out or blur every piece of personal or sensitive data (names, emails, phone numbers, IDs, keys, balances) before anything else.

Rules:
- Keep all annotations inside the original image. Do not extend the canvas.
- Never cover the thing you are pointing at, or another element the text mentions.
- Before delivering, zoom into each annotated area and check placement, overlap and readability.
- Keep the original file untouched; save annotated copies.

If annotating in code, Python with Pillow works well: find the coordinates by cropping and viewing the region first, then draw the line, arrowhead polygon, rounded rectangle and label box.

## Step 3. Assemble and check

- Every step has the screenshot right after the text that describes it.
- Labels in the text match labels in the images.
- No personal data visible anywhere.
- Button names match the current product.
