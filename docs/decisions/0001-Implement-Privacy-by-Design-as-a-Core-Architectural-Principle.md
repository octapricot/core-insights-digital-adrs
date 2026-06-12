# Implement Privacy by Design as a Core Architectural Principle

* Status: accepted
* Date: 2026-06-12

Technical Story: As a platform processing sensitive financial data of EU and UK users across a multi-tenant SaaS architecture with AI-driven profiling, privacy must be embedded into the architecture from day one rather than added as an afterthought.

## Context and Problem Statement

The platform is subject to GDPR and CCPA (CRN-07), processes sensitive financial data across multiple tenants (CRN-09), and uses AI to generate personalized investment recommendations. Privacy violations in this context carry significant regulatory penalties and reputational risk. The legacy system did not have privacy built into its architecture, contributing to cybersecurity incidents (CON-03). The new platform must take a fundamentally different approach.

## Decision Drivers

* GDPR Article 25 mandates Privacy by Design and by Default for systems processing personal data
* Multi-tenant architecture requires strict data isolation between tenants by design
* AI-driven features create additional privacy risks around profiling and automated decision-making
* EU AI Act obligations apply to AI systems making financial recommendations
* CTO mandate for zero-trust security framework aligns naturally with privacy by design principles

## Considered Options

* Privacy by Design: embed privacy requirements into every architectural decision from the start
* Privacy by Compliance: address privacy requirements reactively as compliance checkpoints before release
* Privacy by Policy: rely on organizational policies and user agreements rather than technical controls

## Decision Outcome

Chosen option: "Privacy by Design: embed privacy requirements into every architectural decision from the start", because Privacy by Design is adopted as a core architectural principle. Every architectural decision must be evaluated against privacy requirements including data minimization, purpose limitation, storage limitation, and data subject rights. The Privacy & Data Protection Engineer role is established on the core team to enforce this principle across all workstreams.

### Positive Consequences

* Reduces risk of GDPR violations and associated penalties
* Builds client trust - particularly important for investment firms handling sensitive financial data
* Aligns with zero-trust security framework already mandated by CTO
* Reduces cost of privacy remediation later in the delivery cycle

### Negative Consequences

* Adds complexity and time to architectural decisions
* Requires dedicated Privacy & Data Protection Engineer on the core team
* May slow down some feature delivery decisions where privacy trade-offs need resolution

## Links

* CRN-07
* CRN-09
* CON-03
* CON-04
