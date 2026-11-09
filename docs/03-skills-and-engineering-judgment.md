# 03. Skills and engineering judgment

Forward deployed engineering is ultimately a judgment exercise as much as a technical exercise. The work is not just “use tools well.” It is deciding which problems matter, what constraints are real, and which technical choices are acceptable under uncertainty.

This guide organizes the skills by decisions rather than tools. The emphasis is on judgment.

## 1. Clarifying the problem

What it means:
A good FDE spends time turning a vague request into a concrete workflow description. The real question is usually not “what tool should we use,” but “what problem are we actually solving?”

Why it matters:
Many failed AI projects begin with user requests that are too broad, too vague, or disconnected from the actual work. Without problem clarity, every later decision is noisy.

Concrete example:
A support team says, “We need an AI to answer customer questions.” After discussion, the actual problem is narrower: draft answers from policy documents, with human review, no account changes, and no outbound messaging.

Common mistake:
Skipping the workflow interview and jumping directly to a demo or a model benchmark.

Source context:
Anthropic’s guidance on building agentic systems emphasizes starting with simple, well-scoped solutions rather than unnecessary complexity. That aligns with the need to clarify the real problem before designing a workflow.

## 2. Establishing a baseline

What it means:
Before implementing AI, understand the current process: how work is done today, where delays or errors come from, and what “good” looks like.

Why it matters:
A baseline helps separate a useful improvement from a flashy but low-value demo. It also clarifies whether a workflow is ready for automation or whether ordinary software is enough.

Concrete example:
A support team currently drafts answers by searching documents manually. The baseline is a human reading policy text, checking authority, and composing a response. The AI design should be judged against that baseline, not against an abstract idea of automation.

Common mistake:
Treating model quality as the same thing as workflow value.

## 3. Scoping

What it means:
Deciding where the system begins and ends, what is in or out of scope, and which tasks are safely delegated to automation.

Why it matters:
Most AI failures are not model failures; they are scope failures. A system fails when it is asked to do things outside of its operational envelope.

Concrete example:
If the assistant is banned from modifying accounts, then refunds, balance changes, and account suspensions belong outside the system’s allowed actions.

Common mistake:
Letting the model or the prototype expand without clear boundaries.

## 4. Data and permissions

What it means:
Understanding what documents exist, who is allowed to access them, how they are versioned, and how they are retrieved.

Why it matters:
A system can be technically capable but unusable if it retrieves the wrong policy set, ignores authorization context, or cannot explain its sources.

Concrete example:
The assistant may be allowed to answer questions about refund policy but not to read account-level billing notes or internal HR content.

Common mistake:
Assuming that if a document exists, it is safe or relevant to use.

## 5. Integration

What it means:
Connecting the AI system to the real environment: identity, data, business rules, review workflow, and operational tooling.

Why it matters:
A strong model alone does not produce a deployable product. Integration determines what the model can actually do in context.

Concrete example:
The assistant must know who the user is, what documents are authorized, and which source references are allowed to support a response.

Common mistake:
Building a model-first prototype without securing the surrounding integration layers.

## 6. AI evaluation

What it means:
Defining what success and failure look like through tasks, edge cases, and rubric-based assessment.

Why it matters:
Without evaluation, teams rely on intuition and surprises in production. Anthropic’s eval guidance emphasizes that good evaluations make system behavior concrete before deployment.

Concrete example:
A support assistant should answer clear policy questions correctly, decline when the source is missing, and avoid unauthorized data retrieval.

Common mistake:
Checking only the happy path and ignoring exceptions.

## 7. Reliability

What it means:
Designing for failure modes: missing sources, conflicting documents, tool outages, ambiguous user requests, and prohibited actions.

Why it matters:
Strong AI systems do not only work when everything is perfect. They fail gracefully when the assumptions are wrong.

Concrete example:
If the retrieval service fails, the assistant should say so candidly and avoid guessing.

Common mistake:
Conflating confident output with reliable output.

## 8. Communication

What it means:
Ensuring customer teams, operators, and review stakeholders understand system limits, expected responsibilities, and why decisions were made.

Why it matters:
AI systems fail not only technically but socially when stakeholders cannot interpret or trust the system.

Concrete example:
A policy-drafting assistant should explain that it can propose a response based on approved sources, but it cannot act on behalf of a customer or issue a refund.

Common mistake:
Relying on technical jargon without explaining actual operational consequences.

## 9. Product feedback

What it means:
Recognizing when a customer-specific fix is a local patch and when it should shape a reusable product improvement.

Why it matters:
The most valuable FDE work often converts local pain into broad platform learning.

Concrete example:
A repeated permission bug becomes a reusable authorization integration. Confusing policy versions become a shared document-version handling pattern. Inconsistent review comments become a reusable evaluation rubric.

Common mistake:
Generalizing too early, or failing to generalize at all when the pattern is repeated.

## Applied AI engineering is not model training

This guide distinguishes applied AI engineering from foundational model research or training. Model training is a different activity. An FDE is not automatically expected to train foundation models. The role is often about making strong, reliable systems work in the real world using the right model, workflow, data, and safeguards.

## Related reading

- [01-what-is-a-forward-deployed-engineer.md](01-what-is-a-forward-deployed-engineer.md)
- [02-fde-vs-other-engineering-roles.md](02-fde-vs-other-engineering-roles.md)
- [04-the-deployment-lifecycle.md](04-the-deployment-lifecycle.md)
- [../sources.md](../sources.md)
