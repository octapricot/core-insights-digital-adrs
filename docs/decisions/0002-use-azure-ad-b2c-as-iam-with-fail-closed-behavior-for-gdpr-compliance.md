# Use Azure AD B2C as IAM with Fail-Closed Behavior for GDPR Compliance

* Status: proposed
* Date: 2026-06-12

## Context and Problem Statement

The platform requires a centralized IAM solution supporting RBAC across four user roles and three subscription tiers, Enterprise SSO, and multi-tenant isolation. The CTO mandated Azure AD as the main IAM system (CRN-05) and a zero-trust security framework (CON-03). GDPR requires that personal data is never exposed to unauthorized parties, including during system failures.

## Considered Options

* Azure AD B2C - cloud-native, integrates with existing Azure infrastructure, supports RBAC, SSO, and fail-closed behavior natively
* Auth0 - mature third-party IAM, flexible but introduces additional external vendor dependency
* Custom-built IAM - maximum control but high development cost, security risk, and not viable given time-to-market constraints

## Decision Outcome

Chosen option: "Azure AD B2C", because It aligns with existing Azure investment and team familiarity, supports RBAC and Enterprise SSO natively, and enables explicit fail-closed behavior ensuring no personal or financial data is exposed during system failures - a non-negotiable GDPR requirement within the zero-trust security framework.
