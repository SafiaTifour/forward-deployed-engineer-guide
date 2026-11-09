# Discovery brief

## Context
An illustrative support team wants AI assistance for drafting responses from policy documents.

## User and workflow
- User role: support agent
- Main task: draft a response grounded in approved policy text
- Current process: manual search and drafting
- Desired workflow: retrieve relevant policy, draft answer, cite source, escalate uncertain cases to a human

## Baseline
Current handling is manual and slow. Team leads review drafts for accuracy and consistency.

## Success
A support agent can quickly produce a relevant answer based on approved policy sources with visible references and a clear escalation path when evidence is missing.

## Constraints
- no outbound messaging from the system
- no refunds or account modification actions
- no access to non-approved policy sources
- must cite source documents

## Data
- internal policy documents
- versioned policy sources
- support ticket metadata limited to the user’s authorized queue

## Non-goals
- direct customer communication
- policy authoring
- general web research
- autonomous account actions

## Owner
- policy owner: compliance or support operations
- technical owner: engineering team
- review owner: support lead

## Example outcome
A support agent drafts a response using approved policy language and cites the relevant policy section. If the policy is ambiguous or conflicting, the system asks for human review instead of guessing.
