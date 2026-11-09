# Rollout and handoff template

## Scope
- what is included in the rollout
- what is excluded
- who is allowed to use it

## Owner
- technical owner
- support or operations owner
- escalation contact

## Monitoring
- review rate
- escalation rate
- failure rate
- policy citation quality

## Escalation
- when a human must step in
- what to do when the system is uncertain

## Fallback
- manual process to use if the system is unavailable
- safe degraded mode

## Rollback
- when to disable the workflow
- how to revert to the prior process

## Support
- who handles incidents
- what logs or artifacts are retained
- what constitutes a major outage

## Example
A small support team rolls out a draft-generation tool for policy questions. If the retrieval layer fails or the answer is not grounded, the team reverts to manual draft handling.
