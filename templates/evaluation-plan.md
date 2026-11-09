# Evaluation plan template

## Tasks
- list the key user tasks
- include edge cases and failure cases
- include positive and negative examples

## Failure categories
- missing evidence
- unauthorized access
- ambiguous request
- conflicting policy versions
- prohibited actions
- retrieval failure

## Expected outcomes
- correct answer grounded in approved sources
- correct refusal or escalation when needed
- clear citation or evidence trail

## Graders
- deterministic checks
- model-based assessment
- human review
- release checklist

## Privacy
- what data is allowed in the evaluation set
- how sensitive data is anonymized or excluded
- what telemetry is collected

## Limitations
- this dataset is illustrative
- no production readiness claim is implied

## Example
One task tests a missing-evidence case. The expected outcome is a clear statement that the policy does not provide an answer, followed by escalation to a human reviewer.
