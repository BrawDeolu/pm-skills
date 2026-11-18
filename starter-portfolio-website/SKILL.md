---
name: starter-portfolio-website
description: Build a personal portfolio website for someone early in their career (student, graduate, career switcher), from intake questions to a published, responsive one-page site.
---

# Starter Portfolio Website

Use this skill when someone at the start of their career (student, fresh graduate, intern, NYSC corps member, bootcamp grad, career switcher) wants a portfolio website. The goal is a site that makes a hiring manager think "this person is worth a conversation" within 10 seconds, even when the person has little or no formal work experience.

## Core principles

1. **Evidence over claims.** Beginners have thin CVs, so the site sells proof: projects, coursework, volunteer work, side hustles, competitions, writing. "Built X that did Y" beats "passionate, hardworking team player".
2. **One clear target.** The site is aimed at one kind of role (for example "junior product designer" or "entry-level data analyst"). Everything on the page supports that target.
3. **Never invent anything.** No made-up metrics, employers, testimonials, clients, awards or links. If a detail is missing, ask, or leave a clearly marked placeholder like `[ADD: link to project]` and list every placeholder at the end.
4. **Small and finished beats big and empty.** A strong one-page site with 2 to 4 projects is better than a multi-page site with "Coming soon" sections.

## Step 1: Intake

Ask these questions before building. Ask in small batches (3 to 4 at a time), not one giant form. If the person already shared a CV or LinkedIn, read it first and only ask for what is missing.

**Target**
- What role or field are you aiming for? Any specific companies or industries?
- Where are you based, and are you open to remote or relocation?

**Story**
- In one or two sentences, what do you do and what do you want to do next?
- What makes your path different? (a non-traditional degree, a side business, a self-taught journey, a career switch)

**Proof** (the most important batch)
- List 2 to 6 things you have built, run, designed, written, analysed or led. For each: what was the problem, what did you do, what tools did you use, and what happened as a result?
- Do you have links, screenshots, GitHub repos, Figma files, case studies or write-ups for any of them?
- Any internships, NYSC placements, freelance gigs, volunteer roles, student leadership, hackathons, certifications or awards?

**Practical**
- Name, email, LinkedIn, GitHub/Behance/Dribbble/Medium (whichever fit the field), CV link.
- Do you have a professional photo? (optional)
- Any colours, sites or styles you like or hate?
- Do you already own a domain?

## Step 2: Plan the content

Before designing, write the content outline and confirm it with the person. Use this one-page structure by default:

1. **Hero**: name, a one-line positioning statement, and one primary call to action ("View my work" or "Download CV"). Positioning formula: `[Role you want] who [what you do] for [who / what kind of problem].` Example: "Aspiring product designer who turns messy student workflows into simple mobile apps."
2. **Selected work**: 2 to 4 project cards, strongest first. Each card: title, one-line summary, role, tools, and a link to a case study or the live thing.
3. **About**: 80 to 150 words in first person. Where you are now, how you got here, what you are looking for. One human detail is fine; a life story is not.
4. **Experience and education**: compact timeline. Include internships, NYSC, freelance, volunteering, leadership and relevant courses. Each entry gets one line of what you actually did.
5. **Skills and tools**: grouped (for example "Design", "Research", "Tools"). Only list things they can talk about in an interview. No skill-percentage bars.
6. **Contact**: email (as a mailto link), LinkedIn, and one or two field-relevant profiles. A clear sentence like "Open to junior roles and internships from January".

Optional sections, only if there is real material: Writing, Certifications, Testimonials (real ones with names and permission only), Speaking.

### Project case study format

For the 1 or 2 strongest projects, write a short case study (on the same page as an expandable section, or a separate page):

- **Context**: what was this and why did it exist?
- **Problem**: what was broken or needed?
- **My role**: what *you* did, separated from the team's work.
- **Process**: 3 to 5 key steps or decisions, with visuals if available.
- **Outcome**: what happened. Real numbers if they exist; otherwise qualitative results ("used by my class for a semester", "shipped and presented to judges").
- **What I learned**: one or two honest sentences. Recruiters for junior roles care a lot about this.

### Writing rules

- Plain, confident, first-person English. Short sentences.
- Lead with verbs: built, designed, ran, analysed, launched, led.
- Cut filler words: passionate, hardworking, guru, ninja, rockstar, synergy.
- Do not apologise for being junior. Frame it as "early in my career" once, at most.
- Avoid em dashes in copy; use commas, colons or full stops.

## Step 3: Design and build

If a frontend or design skill is installed, load it before writing code.

Build a single self-contained HTML file (HTML, CSS and a little JS in one file) unless the person asks for a framework. Requirements:

- **Responsive**: looks right at 375px (phone), 768px (tablet) and 1280px+ (desktop). Most recruiters first open links on their phones.
- **Fast**: no heavy libraries, compressed images, system or one or two web fonts at most.
- **Accessible**: semantic HTML (`header`, `main`, `section`, `footer`), alt text on every image, visible focus states, colour contrast at least 4.5:1 for body text, nav usable by keyboard.
- **SEO and sharing basics**: a real `<title>` ("Name, Role"), meta description, Open Graph tags (title, description, image) so links look good on LinkedIn and WhatsApp, and a favicon.
- **Design direction**: pick one clear direction that suits the field (a designer can be bolder; an analyst or engineer can be clean and structured). Use one accent colour, generous whitespace, and a clear type hierarchy. Avoid generic template looks: no stock hero gradients with floating blobs, no skill progress bars, no typing-animation headlines.
- **Content first**: real copy in place from the start, not lorem ipsum. Placeholders follow the `[ADD: ...]` format.
- **Simple nav**: sticky or top nav with anchor links to the sections, plus a visible CV link.
- Light mode by default; dark mode toggle is optional.

## Step 4: Review

Before delivering, check:

- [ ] The 10-second test: from the hero alone, can a stranger tell who this is, what role they want and where to see their work?
- [ ] Every project has a role, tools and an outcome.
- [ ] No invented facts. All placeholders are marked and listed.
- [ ] All links work or are marked as placeholders; email is a mailto link.
- [ ] Looks right at phone, tablet and desktop widths (render and look at screenshots if possible).
- [ ] Spelling and grammar checked; names of tools and companies spelt correctly.
- [ ] Page title, meta description and Open Graph tags filled in.

## Step 5: Deliver and help them go live

1. Give the person the finished HTML file, and show a live preview if the tool you are working in supports one.
2. List every placeholder they still need to fill.
3. Offer free hosting options, one at a time if they want a walkthrough:
   - **GitHub Pages**: free, good for anyone in tech; site at `username.github.io`.
   - **Netlify** or **Vercel**: drag-and-drop or Git deploys, free tier, easy custom domains.
4. Recommend a custom domain (ideally `firstnamelastname.com`) once they are ready, and explain how to point it at their host.
5. Suggest next steps: add the link to their LinkedIn "Featured" section, CV header and email signature; add one new project every few months.

## Things to avoid

- Fabricating metrics, testimonials, clients or employers to make the person look more experienced.
- Listing every course or tool they have ever touched.
- Long paragraphs of personal history in the About section.
- Auto-playing music or video, heavy animations, cursor effects.
- Contact forms that need a backend unless the person sets one up; a mailto link is enough to start.
