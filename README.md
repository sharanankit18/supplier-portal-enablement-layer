# Supplier Portal Enablement Layer — Prototype & Case Study

A product prototype exploring in-product guidance (tooltips, walkthroughs, sandboxes, and AI help) for a supplier-facing onboarding portal in a global enterprise.

---

## TL;DR

- Role: Product Manager, Supply Chain (Sourcing, Contracting, Supplier Lifecycle Management, Procurement).
- What: A clickable prototype of an "enablement layer" for an inhouse-built Supplier Lifecycle Management application. The prototype was used to pressure-test guidance patterns with real business stakeholders.
- How it was built: Prototyped with Claude (AI-assisted design/build); I directed the requirements, defined the workflow scenarios, and made manual edits to the HTML/JS provided by Claude.
- Purpose: Turning an abstract "we should add in-app help" conversation into something stakeholders could interact with and provide feedback.
- Outcome: Structured feedback across guidance patterns in the platform, sorted into a clear _now / later / no_ framework that fed directly into the product roadmap and guided the PRD.

---

## The Case Study

### The problem

During our in-house Supplier Lifecycle Management (SLM) platform development, I wanted to build an application that removed the need for traditional user training methods (user guides, lunch-n-learn sessions, etc.) for both internal and external users. Since there are several ways to solve this, I didn't want to waste any engineering resources to any one of these without validating which ones actually mattered to stakeholders.


### The approach

To gather user feedback, I built a clickable prototype covering distinct guidance patterns, each mapped to a real workflow in the SLM application:

1. Microcopy only: inline field-level help and explanatory validation (low complexity, high frequency)
2. Wizard + walkthrough + sandbox + video + KB + AI: the "everything" option, for high-complexity workflows
3. Pre-login demo + checklist + lifecycle email nudges: for quick training of suppliers before their first login
4. Role-based learning path + certification quiz: for auditable training for roles with sensitive data access
5. Knowledge base + AI assistant only: a lighter-weight, self-serve option

I also prototyped an authoring/admin console showing how a non-engineering team member could maintain this guidance content directly, so rolling out new features wouldn't require new engineering effort just to update in-app help.

Each pattern was presented as a set of annotated, realistic screens (not wireframes) so stakeholders could react to something concrete rather than a description.


### The tool

The prototype itself was built using _Claude (Anthropic's AI assistant)_ I specified the requirements, features, the guidance patterns, and the interaction logic, and iterated on the generated HTML/JS manually where I knew enough front-end code to adjust behavior. This allowed me to go from generic questions to a reviewable, interactive artifact in days rather than waiting on a design/dev cycle for something that was explicitly meant to be thrown away or kept, depending on the feedback.


### The feedback framework

I walked stakeholders through the prototype across the business and engineering side, and asked them to react to each of the guidance patterns independently using a simple 3-way feedback format:

|          Signal          |                       Meaning                       |    
|--------------------------|-----------------------------------------------------|
| Yes, I want it           | Clear demand, prioritize for near-term roadmap      |
| Good, but maybe later    | Validated value, not urgent, backlog candidate      |
| Too much / no clear use  | Cut, avoid building something with no adoption path |

This turned a fuzzy "user need help" ask into a ranked, evidence-based set of roadmap candidates rather than a guess.

### Outcome

- The feedback directly shaped which enablement patterns made it into the SLM roadmap and which were explicitly deprioritized.

---

## How to view it

This is a static, self-contained HTML/JS prototype — no build step, no server required.

```bash
git clone https://github.com/sharanankit18/supplier-portal-enablement-demo.git
cd supplier-portal-enablement-demo
open src/index.html   # or just double-click the file
```

---

## Repo structure

```
supplier-portal-enablement-demo/
├── README.md
├── LICENSE
├── .gitignore
├── src/
│   ├── index.html
│   └── support.js└── screenshots/
    └── screenshots of the prototype
```

---

## Notes on scope

This is a prototype built to gather feedback and validate direction, not production code, and not connected to any live system or real supplier data. All company names, URLs, and identifying details have been removed.

## License

MIT — see [LICENSE](./LICENSE).
