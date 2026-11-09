# Forward Deployed Engineering, Explained

A source-backed guide to the role, with a worked AI deployment scenario, evaluation examples, and reusable templates.

## What is a Forward Deployed Engineer?

A Forward Deployed Engineer is a customer-facing engineering and delivery model: someone who works close to a real operational problem, helps implement a solution, and then feeds what was learned back into product and platform work. In plain language, it is not just a collection of AI frameworks or a catchy title. It is a way of organizing work around the practical realities of customer environments, constraints, and operational bottlenecks.

The phrase “forward deployed” means the engineer is not only building in a lab or a product team; they are placed near a problem and often working with customers, domain experts, operators, or internal stakeholders to understand what is actually painful, risky, or inefficient in context. The role is therefore shaped by customer proximity, implementation, and the pressure to turn a narrow problem into something reliable enough to use.

An FDE typically does work across discovery, scoping, system design, implementation, rollout, evaluation, and operational feedback. In many employer descriptions, the work includes helping embed a technical solution into a real workflow rather than merely shipping a prototype. That is a useful distinction: the point is not just to write code, but to make a real deployment workable under constraints.

## What makes it different from adjacent roles?

A software engineer usually designs, builds, and maintains software in a product or platform context. An AI engineer often focuses on model integration, workflows, experimentation, or applied ML systems. A solutions engineer may consult on fit, architecture, and customer adoption. A Forward Deployed Engineer often sits closer to the actual delivery problem, has more direct ownership of the implementation path, and is expected to influence reusable product direction based on field experience.

The boundaries are not universal. Titles vary, and organizations impose different mixes of implementation, customer work, and product feedback. The role is best understood as a delivery model with customer proximity rather than a rigid, single job description.

The guide’s synthesis is that FDE is often a specific kind of product-engineering and delivery work: it emphasizes close contact with real operational environments, turning fuzzy workflows into something that works in production, and feeding those lessons back into the broader platform.

This distinction matters in AI work. Not all forward deployed engineering is AI work, and not all production AI engineering is forward deployed engineering. A company may run AI deployments without using an FDE model, and a company may use forward-deployed engineering in non-AI contexts. This is a synthesis based on the role descriptions and platform documentation reviewed here rather than a universal industry definition.

## Why does the role matter for AI deployments?

The role matters because AI systems do not succeed by model quality alone. They depend on real data access, authorization, workflow constraints, user trust, testing, integration, and operational reliability. The more a deployment touches business processes or high-stakes work, the more it matters to understand the workflow, risk, and change management around the system.

A model can be impressive in isolation and still fail in deployment because the surrounding system is brittle. A support assistant may draft useful answers but fail if it cannot retrieve the right policies, lacks authorization, or produces confident but unsupported claims. An FDE works on that boundary: translating technical capabilities into an operationally usable system while feeding real friction back into product and engineering improvements.

Customer problem → implementation → observed friction → reusable improvement → core product is a useful shorthand for the product feedback loop. The model and the workflow are both shaped by real user needs. The work of an FDE is often a mechanism to convert a narrow, customer-specific problem into something reusable.

## How responsibilities vary across employers

The role varies substantially between employers. Some companies describe FDEs as close to product and customer delivery. Others emphasize platform integration, security, and deployment. The Palantir architecture material highlights a model where engineering teams near customer problems generate feedback that is synthesized into platform improvements, while the Sovereign AI reference architecture distinguishes infrastructure and model work from workflow and platform work. The OpenAI job description emphasizes end-to-end deployment, scoping, system design, rollout, and feedback into product and research roadmaps. That variety is important to recognize: FDE is not a single universal template.

The practical takeaway is that the role can range from highly application-focused to platform-adjacent, depending on the employer, product, and customer context. The common thread is customer proximity and a bias toward shipping workable systems in real conditions.

## A short example

A support team wants help drafting responses from internal policy documents. A basic workflow might be: identify the user, check authorization, retrieve the relevant policy text, draft a response grounded in the cited sources, and route the result for human review. The system is constrained: it cannot send emails, issue refunds, or access unrelated data. This is a realistic early-stage AI deployment because it solves a narrow pain point with clear guardrails. It is not “agentic” simply because it uses an LLM; it is a constrained retrieval-and-drafting workflow designed to reduce writing overhead while preserving accountability.

The worked scenario in this repository uses this example throughout, along with a fictional fictional support assistant. It is deliberately illustrative and not a real client engagement.

## Worked scenario and reusable artifacts

This repository includes a concrete walkthrough built around a support assistant, plus templates for discovery, evaluation, rollout, and decision records. The goal is to make the ideas actionable without requiring a real production system.

- Start with the README and then read the deeper guide pages.
- Review the support-assistant scenario for a realistic end-to-end example.
- Use the templates to structure discovery, evaluation, and handoff work.
- Check the source ledger before treating any claim as settled.

## Scope and limitations

This repository is designed to explain the role and the deployment model clearly, not to promise a career path, certification, or industry consensus. It synthesizes public role descriptions, practitioner perspective, and engineering guidance, and it is a documentation project rather than an enterprise-ready product.

It does not claim the author worked as an FDE, served clients, led deployments, interviewed candidates, or obtained expert review. It is written with technical clarity and practical judgment, not invented authority.

## Contributions and review

Contributions are welcome when they improve clarity, evidence quality, or usefulness. Please read [CONTRIBUTING.md](CONTRIBUTING.md) and use the issue templates in [.github/ISSUE_TEMPLATE](.github/ISSUE_TEMPLATE) for factual corrections or resource suggestions.

## Methodology note

The guide synthesizes public role descriptions, practitioner perspectives, and engineering documentation. Its worked example and templates are illustrative. AI assistance was used to draft and refine the repository outline and prose, but the content is written to be source-aware, explicit about uncertainty, and intentionally conservative where sources are limited or inaccessible.

## Recommended reading

- [docs/01-what-is-a-forward-deployed-engineer.md](docs/01-what-is-a-forward-deployed-engineer.md)
- [docs/02-fde-vs-other-engineering-roles.md](docs/02-fde-vs-other-engineering-roles.md)
- [docs/03-skills-and-engineering-judgment.md](docs/03-skills-and-engineering-judgment.md)
- [docs/04-the-deployment-lifecycle.md](docs/04-the-deployment-lifecycle.md)
- [walkthrough/support-assistant/README.md](walkthrough/support-assistant/README.md)
- [templates/discovery-brief.md](templates/discovery-brief.md)
- [sources.md](sources.md)
