Supplier Portal Enablement Layer — Prototype & Case Study

A product prototype exploring in-product guidance (tooltips, walkthroughs, sandboxes, and AI help) for a supplier-facing onboarding portal in a multi-national QSR enterprise.

---

TL;DR

- Role: Product Manager — Supply Chain (Sourcing, Contracting, Supplier Lifecycle Management, Procurement)
- What: A clickable prototype of an "enablement layer" for an internally-built Supplier Lifecycle Management application. The prototype was used to pressure-test guidance patterns with real business stakeholders.
- How it was built: Prototyped with Claude (AI-assisted design/build); I directed the requirements, defined the workflow scenarios, and made manual edits to the HTML/JS provided by Claude.
- Purpose: Turning an abstract "we should add in-app help" conversation into something stakeholders could interact with and provide feedback.
- Outcome: Structured feedback across guidance patterns in the platform, sorted into a clear _now / later / no_ framework that fed directly into the product roadmap and guided the PRD.

---

The Case Study

The problem

During our in-house Supplier Lifecycle Management (SLM) platform development, there an ask to move away from traditional user training methods (user guides, lunch-n-learn, etc.) But the requirements were vague. Business kept asking _"users want access to help when they need it"_, or _"suppliers do not want to go through screenshot-based user-guides and try to find how to use the system"_.
As these are not actionable requirements on their own, committing engineering time to any one of these without validating which ones actually mattered to stakeholders risked wasted of resources.

The approach

Rather than write a PRD off of a vague ask, I built a clickable prototype covering distinct guidance patterns, each mapped to a real workflow in the SLM application:

1. Microcopy only — inline field-level help and explanatory validation (low complexity, high frequency)
2. Wizard + walkthrough + sandbox + video + KB + AI — the "everything" option, for high-complexity workflows
3. Pre-login demo + checklist + lifecycle email nudges** — for quick training of suppliers before their first login
4. Role-based learning path + certification quiz** — for auditable training for roles with sensitive data access
5. Knowledge base + AI assistant only — a lighter-weight, self-serve option

An additional interface to maintain the training materials was also build. This is to ensure that as new features are rolled out, training admins can keep in-application guidance up-to date

Each pattern was presented as a set of annotated, realistic screens (not wireframes) so stakeholders could react to something concrete rather than a description.

### The tool

The prototype itself was built using **Claude** (Anthropic's AI assistant) — I specified the workflows, the guidance patterns, and the interaction logic, and iterated on the generated HTML/JS manually where I knew enough front-end code to adjust behavior. This let me go from "vague ask" to a reviewable, interactive artifact in days rather than waiting on a design/dev cycle for something that was explicitly meant to be thrown away or kept, depending on the feedback.

### The feedback framework

I walked the prototype through stakeholders across the business and engineering side, and asked them to react to **each of the five patterns independently** using a simple 3-way sort:

| Signal | Meaning |
|---|---|
| ✅ **Yes, I want it** | Clear demand, prioritize for near-term roadmap |
| 🕒 **Good, but maybe later** | Validated value, not urgent — backlog candidate |
| ❌ **Too much / no clear use** | Cut — avoid building something with no adoption path |

This turned a fuzzy "suppliers need help" ask into a **ranked, evidence-based set of roadmap candidates** rather than a guess.

### Outcome

- The feedback directly shaped which enablement patterns made it into the SLM roadmap and which were explicitly deprioritized.
- [Add 1–2 sentences here on concrete impact once you're comfortable sharing it, e.g. "Pattern 1 and 5 were greenlit for Q_ delivery; pattern 2 was scoped down to a smaller subset."]
- More broadly, this validated a pattern for how I gather requirements going forward: build a prototype fast with AI assistance, use it as a shared artifact for structured feedback, and let that evidence — not the loudest voice in the room — drive prioritization.

### What I'd do differently

- [Optional: add a short, honest retro note — e.g. "I'd test with a broader supplier-side sample, not just internal stakeholders" or "I'd quantify effort next to each option so the trade-off was explicit during scoring."]

---

## How to view it

This is a static, self-contained HTML/JS prototype — no build step, no server required.

```bash
git clone https://github.com/<your-username>/supplier-portal-enablement-demo.git
cd supplier-portal-enablement-demo
open src/index.html   # or just double-click the file
```

Or use any static file server, e.g. `npx serve src`.

---

## Repo structure

```
supplier-portal-enablement-demo/
├── README.md
├── LICENSE
├── .gitignore
├── src/
│   ├── index.html          # the prototype
│   └── support.js          # supporting logic/runtime for the prototype
└── docs/
    └── screenshots/        # optional: a few PNGs or a GIF of the prototype in action
```

---

## Notes on scope

This is a prototype built to gather feedback and validate direction — not production code, and not connected to any live system or real supplier data. All company names, URLs, and identifying details have been genericized.

## License

MIT — see [LICENSE](./LICENSE).
