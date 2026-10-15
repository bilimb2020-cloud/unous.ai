# unous.ai — project instructions for Claude

## Design workflow (always applies)

Whenever a task involves design — UI, UX, visual identity, landing pages,
product flows, or naming/branding — do NOT design from memory alone:

1. First invoke the `design-research` skill (`.claude/skills/design-research/SKILL.md`).
   It requires researching current and related-field design concepts via web
   search **before** proposing or building a design. Do this proactively,
   without the user asking for research.
2. Read `docs/design/design-concepts.md` (the living research reference) and
   check its "Last updated" date. If it is more than ~2 months old, or the
   task touches an area it doesn't cover, run fresh searches and update it.
3. Only then propose/build the design, citing which concepts you applied and why.

## General

- The user is bilimb2020@gmail.com (GitHub: bilimb2020-cloud).
- Keep deliverables in the repo so they persist across cloud sessions.
