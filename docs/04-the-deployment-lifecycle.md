# 04. The deployment lifecycle

This chapter proposes a practical lifecycle for understanding how a customer problem becomes a deployable system. It is a guide’s organizing framework rather than a universal industry standard.

## Discovery

The first step is to understand the actual workflow: what the user is trying to do, where the friction is, and which constraints matter. This is where vague requests become testable requirements.

## Scope

The project is then bounded: what is in-scope, what is out-of-scope, and what decisions must stay with the human. This stage clarifies where automation is useful and where it should not be used.

## Thin end-to-end prototype

Before investing heavily in infrastructure or rollout, build a minimal system that can demonstrate the core workflow. The prototype should test whether the real use case is feasible in a plausible environment.

## Evaluation

Evaluation is where the team defines what acceptable behavior looks like. This includes not only success cases but also edge cases: missing evidence, conflicting policies, ambiguous requests, or unauthorized access. The goal is to separate actual improvement from a convincing demonstration.

## Hardening

Once the workflow is promising, the team hardens the system: access control, retrieval reliability, output grounding, failure behavior, and human review. This is where a prototype becomes a more defensible operational system.

## Limited rollout

Deploy in a constrained environment with clear ownership, monitoring, and feedback channels. This stage reduces the chance of broad operational disruption while still testing real behavior.

## Operations

Operations includes the regular checks that keep the system usable: monitoring, support, escalation, fallback behavior, data freshness, and user feedback. Production AI is not “set and forget.”

## Product feedback

The final step is to convert the customer-specific learning back into reusable product or operational improvements. This can include better authorization patterns, data models, versioning, evaluation rubrics, or workflow design that benefit future deployments.

## When ordinary software is enough

A plain rules-based workflow may be the right answer when the problem is narrow, deterministic, and well-understood. If the work is mostly structured, the maintenance burden is low, and the task does not require flexible interpretation, ordinary software often remains the best choice.

## When retrieval may help

Retrieval is valuable when the decision depends on a large, policy-rich, or frequently changing document set. If the system must answer based on approved text and the right answer depends on the source material, retrieval can be an appropriate augmentation.

## When a fixed workflow is preferable

A constrained, fixed workflow is often better than a free-form agent when the task is narrow, safety-sensitive, and reviewable. In these cases, the benefits of predictability and explicit guardrails outweigh the flexibility of open-ended autonomy.

## When an agent may be justified

An agent may be justified when the task is genuinely open-ended, the environment is sufficiently instrumented, the success criteria are clear, and the team has strong evaluation and supervision mechanisms. Even then, this should be a product decision based on evidence, not a default assumption that more autonomy is better.

## What evidence would change the choice?

The right design depends on several things:
- task complexity
- data quality and freshness
- user trust and review needs
- operational risk
- authorization constraints
- evaluation quality
- cost and latency trade-offs

A team should revisit the choice when the system appears to need more autonomy or when a narrow workflow repeatedly fails because the task definition is too broad.

## Related reading

- [03-skills-and-engineering-judgment.md](03-skills-and-engineering-judgment.md)
- [../walkthrough/support-assistant/README.md](../walkthrough/support-assistant/README.md)
- [../sources.md](../sources.md)
