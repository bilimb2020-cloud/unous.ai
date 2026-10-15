---
name: design-research
description: Research-first design workflow. Use BEFORE any design task — UI/UX design, visual or brand identity, landing pages, dashboards, product flows, component design, redesigns, or "make it look better" requests. Searches the web for current trends, related-field concepts, and newer patterns, then applies them to produce a stronger, up-to-date design. Trigger proactively whenever the user asks to design, build, style, or improve anything visual or experiential — the user does not need to ask for research.
---

# Design research workflow

The goal: never design from stale memory. Every design starts from fresh,
targeted research, then synthesizes it into a design that fits this project.

## Step 1 — Frame the design problem (1 minute, no tools)

Write down, briefly:
- What is being designed (artifact type: landing page, app screen, flow, brand, …)
- Who it's for and what feeling/outcome it must produce
- Constraints (existing design tokens in this repo, tech stack, accessibility)

## Step 2 — Research (always, proactively)

Run web searches in parallel (3–5 queries, standard mode; extended mode for
fast-moving trend topics). Cover **three angles**:

1. **Current state of the art** for this artifact type
   (e.g. "SaaS onboarding flow design patterns <current year>").
2. **Related / adjacent fields** — deliberately search one or two fields next
   to the problem, where stronger ideas often live:
   - game UI → feedback, juice, progression
   - editorial/print design → typography, grids, hierarchy
   - data visualization → encoding, density, legibility
   - industrial design / architecture → affordances, material honesty
   - motion design / film → pacing, transitions, attention
3. **Newer concepts** that postdate training data — search
   "<topic> trends <current year>" and "<topic> <next year>". For AI products
   specifically, check for new agentic-UX and generative-UI patterns
   (controlled / declarative / open-ended tiers, AG-UI, A2UI and successors).

Also read `docs/design/design-concepts.md` for the project's accumulated
reference, and check actual acclaimed examples (awwwards, siteinspire, land-book,
mobbin — fetch a couple if reachable) rather than only trend listicles.

## Step 3 — Synthesize before designing

Produce a short concept brief (in the deliverable doc or PR description, not
just chat):
- 3–6 concepts/patterns chosen from the research, each with one line on *why
  it fits this problem* — discard trends that don't serve the user or content.
- 1–2 deliberate points of personality (where the design diverges from the
  current default look, so it doesn't feel template-generated).
- Non-negotiables: WCAG 2.2 AA contrast (4.5:1 body text, 3:1 UI), keyboard
  navigation and focus states, reduced-motion support, mobile-first layout.

## Step 4 — Design, then write back

- Build the design applying the brief. Prefer semantic design tokens
  (primitive → semantic layering), a modular type scale, and an 8px spacing
  grid unless the repo already defines its own system.
- Append anything genuinely new you learned to `docs/design/design-concepts.md`
  (with date and source links) and refresh its "Last updated" date, so the
  next session starts smarter.

## Anti-patterns

- Skipping research because the task "seems simple" — a button redesign still
  gets at least one search.
- Trend-stacking: applying every 2026 trend at once. Pick what serves the content.
- Citing trends without sources or dates in the written brief.
