# Architecture decision record template

## Context
- what problem prompted the decision
- what constraints are driving the solution

## Options
- option A: simple workflow
- option B: more autonomous agent
- option C: manual process

## Decision
Describe the selected option and why it was chosen.

## Trade-offs
- benefits
- costs
- risks
- operational complexity

## Evidence
- user interviews
- eval results
- errors and edge cases observed

## Revisit conditions
- when the system grows beyond scope
- when evidence indicates the current design is insufficient
- when operational risk changes

## Example
The team chooses a constrained retrieval-and-drafting flow because the system is narrow, reviewable, and policy-dependent. The decision is revisited if later evidence shows the workflow is being stretched beyond its safe boundaries.
