# Architecture notes

## High-level design
The illustrative architecture is intentionally narrow and specifically not a production deployment.

## Components
- Identity layer: authenticates the user and provides authorization context.
- Document retrieval layer: accesses approved policy sources only.
- Generation layer: writes a draft response grounded in the relevant text.
- Source reference layer: attaches policy citations or snippets to the response.
- Human review layer: final answer is reviewed before use.
- Telemetry layer: records privacy-aware metrics, events, and failure modes.

## Authorization requirements
The system must verify:
- which documents the user can access
- whether the request maps to a supported workflow
- whether the answer requires escalation or review

## Missing evidence handling
When required evidence is absent or ambiguous, the answer should state the limitation and ask for review rather than manufacturing a confident response.

## Privacy-aware telemetry
Telemetry must avoid storing sensitive customer data or raw account content beyond what is necessary for operational monitoring. It should track failures, policy fallback states, and review rates without capturing unnecessary personal information.

## What this repository implements
This repository includes the documentation and design patterns, not a functioning deployed application.

## What a future version might require
A production system would need hardened deployment controls, security review, operational monitoring, and perhaps a more formal evaluation suite.
