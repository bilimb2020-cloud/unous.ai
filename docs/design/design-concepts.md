# Design concepts — living research reference

**Last updated: 2025-10-15.** Refresh (per the `design-research` skill) when
this is >~2 months old or a design task touches an area not covered here.
Append new findings with dates and sources; prune entries that stop being true.

This is a reference of current design concepts gathered from web research,
weighted toward what an AI product (unous.ai) is likely to need. It is
directional, not gospel — most sources are practitioner/agency writing.

---

## 1. Overall direction for 2025–2026

The consensus across trend roundups: the pendulum is swinging from visual
theatrics toward **calm, legible, trust-building interfaces** — especially for
AI products, where users arrive skeptical.

- **Calm design / cognitive clarity** — lower cognitive load, fewer competing
  effects; motion exists to give feedback, not to decorate.
- **Transparent, overridable AI** — AI-native UI where the user can see what
  the system did and override it; trust is the scarce resource.
- **Visible structure** — grids and monospaced type used as part of the final
  visual language ("function-forward"), not hidden scaffolding.
- **Expressive counterweights** — kinetic/variable typography, broken/organic
  grids, neo-brutalism, Y2K revival, bold saturated palettes. Used as accents
  of personality against otherwise minimal layouts.
- **Material styles** — glassmorphism matured into "liquid glass" (Apple's
  2025 direction); a subtle skeuomorphism (soft shadows, gentle gradients) is
  returning.
- **Fluid type** — type scales that interpolate with viewport size
  (`clamp()`-based), replacing fixed breakpoint jumps.
- **3D & scroll storytelling** — WebGL product views, scroll-driven animation
  (now a native CSS capability) — used sparingly and with `prefers-reduced-motion`.
- **Accessibility as baseline, not feature** — WCAG 2.2 AA is table stakes;
  the European Accessibility Act (in force June 2025) makes it a legal
  requirement for many products serving the EU.

Sources: [Envato — UX/UI trends 2026](https://elements.envato.com/learn/ux-ui-design-trends),
[Envato — web design trends 2026](https://elements.envato.com/learn/web-design-trends),
[Musemind — 23 UI trends](https://musemind.agency/blog/ui-design-trends),
[Tubik Studio — 7 UI trends 2026](https://tubikstudio.com/blog/ui-design-trends-2026/),
[WebFX — UX/UI trends](https://www.webfx.com/blog/web-design/ux-ui-trends/),
[UX Pilot — web design trends 2026](https://uxpilot.ai/blogs/web-design-trends-2026).

## 2. AI product UX (agentic + generative UI)

Most relevant field for unous.ai. Chat alone is considered insufficient
("nobody wants another chatbot"); the emerging practice:

- **Generative UI has three tiers** (trade predictability for flexibility):
  1. **Controlled** — the agent selects from a developer-built component
     library. Predictable, testable; limited range.
  2. **Declarative** — the agent emits a structured spec the frontend renders
     (Google's **A2UI** is the reference spec). Middle ground; no arbitrary
     code execution.
  3. **Open-ended** — the agent generates HTML/JSX in a sandbox. Max range;
     styling, security and performance risks.
- **AG-UI protocol** is the common runtime/event layer under agent↔frontend
  interaction; design agentic UX around the **event model** (what the agent is
  doing now) rather than around a component library.
- **Agent UX essentials**: show live progress, let users **intervene
  mid-task**, always provide recovery/undo paths, and stream partial results
  instead of blocking on completion.
- Adoption signal: Google rebuilt parts of Search around generative UI (2026);
  Gartner projects 40% of enterprise apps embedding task-specific agents by
  end of 2026.

Sources: [CopilotKit — generative UI guide](https://copilotkit.ai/blog/the-developer-s-guide-to-generative-ui-in-2026),
[AI Accelerator Institute — 7 interface architectures](https://www.aiacceleratorinstitute.com/nobody-wants-another-chatbot-7-interface-architectures-worth-building/),
[Infosys — agentic UI patterns](https://blogs.infosys.com/digital-experience/mobility/agentic-ui-patterns-designing-frontends-that-collaborate-with-ai-agents.html),
[Aufait UX — agentic AI design patterns](https://www.aufaitux.com/blog/agentic-ai-design-patterns-guide/).

## 3. Design-system foundations (defaults for this repo)

Unless a task demands otherwise, build on:

- **Layered tokens**: primitive values → global tokens → **semantic tokens**
  (brand/success/warning/error, surface/text/border, state variants). Theme
  switching happens at the semantic layer.
- **Type**: modular scale (ratio-based), fluid via `clamp()`; practical range
  ~12–80px in coherent steps.
- **Spacing**: 8-point grid (4px half-steps where needed) for margin, padding, gap.
- **Color contrast**: ≥4.5:1 body text, ≥3:1 large text and UI elements.
- **Also tokenized**: radius, shadow/elevation, motion durations + easing.
- **Dark mode from day one** — define both themes at the semantic-token layer,
  with an explicit background on `body`.

Sources: [Figr — creating design-system foundations](https://figr.design/blog/design-system-introducing-design-tokens),
[BC Gov design system foundations](https://www2.gov.bc.ca/gov/content/digital/design-system/foundations),
[Hover design system](https://design-system.hover.to/foundation).

## 4. AI startup landing pages

- **Clarity over hype**: the best AI sites don't try to *look like AI*; they
  make the product feel clear, credible, valuable. Explain what it does in the
  first viewport.
- **Trust fast**: skeptical visitors convert in seconds or leave — concrete
  product storytelling (real UI, real output) beats abstract neural-network
  visuals.
- **Restrained visual identity**: clean layout, generous whitespace, subtle
  motion; dark mode + gradient accents is the current default look — fine as a
  base, but add one deliberate point of personality so it doesn't read as a
  template.
- **Make the abstract tangible**: for agent-style products, show the agent
  working (demo, animated walkthrough) — the #1 failure is visitors leaving
  without understanding what the product does.
- **Every section earns its place** and moves toward one primary CTA.

Sources: [Veza Digital — best AI website designs 2026](https://www.vezadigital.com/post/best-ai-website-design-examples),
[Ebaq Design — AI startup landing pages](https://www.ebaqdesign.com/blog/ai-startup-landing-page-examples),
[ControlF5 — AI startup web trends 2025](https://controlf5.in/?p=69096).

## 5. Related-field idea bank

Fields to raid when a design needs an edge (see skill, Step 2):

| Field | What it teaches |
|---|---|
| Game UI | Feedback "juice", progression, reward loops |
| Editorial / print | Typographic hierarchy, grids, pacing of a long read |
| Data visualization | Honest encoding, density without clutter |
| Industrial design | Affordances, material honesty, durability of form |
| Motion design / film | Pacing, transitions, directing attention |

---

## Changelog

- **2025-10-15** — initial research pass (2026 trend roundups, generative-UI
  tiering, token foundations, AI landing-page practice).
