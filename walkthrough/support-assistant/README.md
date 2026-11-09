# Worked scenario: support assistant

This section is an illustrative scenario, not a real client engagement.

## Problem statement

A support team wants help drafting answers from policy documents. The assistant cannot send messages, issue refunds, or modify accounts. It operates within a tightly constrained workflow: answer questions using approved policy sources, cite the sources, and escalate to a human reviewer when the evidence is uncertain.

## Original vague request

> “Can you build an AI support assistant that helps us answer customer issues faster?”

## Questions that expose the real workflow

The vague request hides several critical questions:
- Who is the user?
- Which policies are relevant?
- What is the allowed action set?
- What happens when evidence is missing?
- Who reviews the answer before it is sent?
- How is a draft different from a final response?

## Intended users

The intended users are support agents and team leads, not customers directly. The system supports the human operator by drafting a grounded answer from approved policy text. It should not act independently on customer accounts.

## Current baseline

Today, support agents manually read policy documents, cross-check versions, and draft responses. The process is slow, repetitive, and prone to inconsistency when policies change or are ambiguous.

## Data ownership and freshness

The repository does not implement a live AI application. The scenario assumes that:
- the organization owns the policy documents
- the document set is versioned and maintained by a policy team
- policy documents are refreshed on a documented schedule
- stale content is clearly marked and excluded from retrieval when outdated

## Permissions

The assistant must know:
- who the user is
- which support queue they belong to
- whether they are allowed to access the relevant policy set
- whether the request is in scope for the workflow

## Scope and non-goals

In-scope:
- drafting responses based on approved source documents
- citing policy text and relevant references
- flagging missing or conflicting evidence
- routing to human review when the answer is uncertain

Out-of-scope:
- account changes
- refunds
- sending messages directly
- general web browsing for policy data
- unauthenticated access to internal records

## Architecture decisions

This is a constrained retrieval-and-drafting workflow rather than an open-ended agent. The design is intentionally narrow for reliability. It includes:

- user identity and authorization context
- authorized document retrieval
- answer generation grounded in policy text
- source references for each answer
- missing evidence handling
- human review before sending a final answer
- privacy-aware telemetry

This is the proposed design. The repository itself does not contain a deployed system and should not be read as a production application.

## Failure handling

The workflow should fail in a controlled way when:
- the retrieval service is unavailable
- policy documents conflict
- the user asks something outside scope
- the requested facts are missing from approved sources
- the policy version is unclear or outdated
- the user tries to elicit a disallowed action

Failure modes should be explicit and user-safe. The system should not guess when the evidence is weak.

## Evaluation

The system should be evaluated on:
- answer quality from approved policies
- whether the answer cites valid sources
- whether the assistant refuses disallowed requests
- whether it handles missing or conflicting evidence correctly
- whether human review is triggered when needed

The evaluation cases in this repository cover these patterns in synthetic form.

## Rollout

Rollout should be gradual and limited. Start with a small support team, clear review procedures, and a narrow set of allowed tasks. Track whether downstream reviewers trust the drafts and whether policy quality is maintained.

## Maintenance ownership

The workflow requires operational ownership across:
- policy document stewardship
- access control and authorization
- retrieval pipeline maintenance
- evaluation updates
- review process design
- incident handling

## Product feedback

This scenario can produce reusable product learning. For instance:
- repeated permission errors may lead to a reusable authorization integration
- conflicting policy versions may lead to a shared document-versioning pattern
- inconsistent reviewer comments may become a reusable evaluation rubric

These are hypothetical examples, not statements about a real production deployment.

## Why not an agent from the start?

The system is intentionally not framed as an autonomous agent because the task is narrow, safety-sensitive, and often better handled by deterministic workflow boundaries. More autonomy may be justified later if the team has evidence that the system can reliably handle edge cases, source quality, and human review at scale. Until then, a constrained retrieval-and-drafting workflow is the more appropriate first step.

## Related files

- [architecture.md](architecture.md)
- [discovery-brief.md](discovery-brief.md)
- [evaluation-plan.md](evaluation-plan.md)
- [failure-modes.md](failure-modes.md)
- [rollout-and-handoff.md](rollout-and-handoff.md)
- [product-feedback.md](product-feedback.md)
- [../../templates/discovery-brief.md](../../templates/discovery-brief.md)
