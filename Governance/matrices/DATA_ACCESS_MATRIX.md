# Data Access Matrix

This document defines the data classifications used in TeachLink Mobile, the roles that interact with that data, and the allowed access for each role. It is the versioned reference for data access governance and is self-contained within the `Governance/` folder.

## Scope

This matrix applies to all data processed, retained, or transmitted by the TeachLink Mobile application and its supporting infrastructure. It covers development, staging, and production environments.

## Data Classifications

Data is classified into four tiers. Each tier implies a different level of sensitivity and thus a different default access posture.

| Classification | Description | Examples |
| --- | --- | --- |
| **Public** | Data intended for open disclosure. | Marketing content, public course catalog, release notes. |
| **Internal** | Non-sensitive operational data limited to the team. | Aggregated usage metrics, build logs, feature-flag state. |
| **Confidential** | Personally identifiable information (PII) and account data. | Name, email, role in course, device identifiers, auth tokens. |
| **Restricted** | Highly sensitive data whose disclosure carries legal or significant operational risk. | Credentials, payment details, audit trails, security incident records. |

## Roles

Roles are defined by the governance model in this repository. For the purpose of this matrix, the relevant roles are:

| Role | Description |
| --- | --- |
| **Public / Anonymous** | Unauthenticated users of the app. |
| **Learner** | Authenticated end user accessing their own account and course data. |
| **Instructor** | Authenticated user who manages courses and learner progress. |
| **Contributor** | Anyone with merge access to the repository via a pull request. |
| **Maintainer** | Reviewers with merge and release authority. |
| **Security Officer** | Responsible for vulnerability handling and incident response. |
| **System / Service** | Automated services and background jobs operating with scoped credentials. |

## Access Matrix

The table below specifies the allowed access per role for each data classification. Legend:

- **Read** — can view the data.
- **Write** — can create or modify the data.
- **Delete** — can remove the data.
- **None** — no access is permitted.

| Role | Public | Internal | Confidential | Restricted |
| --- | --- | --- | --- | --- |
| Public / Anonymous | Read | None | None | None |
| Learner | Read | None | Read (own records only) | None |
| Instructor | Read | Read | Read (assigned learners) | None |
| Contributor | Read | Read (dev/staging) | None | None |
| Maintainer | Read | Read, Write | Read (dev/staging), Write (dev/staging) | None |
| Security Officer | Read | Read | Read | Read, Write |
| System / Service | Read | Read, Write | Read, Write (scoped) | Read (scoped), Write (audit only) |

## Enforcement Rules

- Access to **Confidential** and **Restricted** data must be mediated by authentication and authorization checks in the application and backend services.
- **Restricted** data access must be logged to an audit trail that is itself classified as **Restricted**.
- System / service accounts use the principle of least privilege and must be scoped to the minimum data needed for their function.
- No role may read or write data outside its assigned scope, even within a permitted classification.
- **Confidential** data must not be copied into **Internal** or **Public** systems without anonymization or aggregation.

## Review Cadence

This matrix is reviewed on a schedule and on event:

- **Quarterly review** — the Security Officer and Maintainers confirm the matrix still reflects the app and infrastructure.
- **Event-driven review** — any change that introduces a new data classification, role, or data flow must update this document in the same pull request.
- **Annual attestation** — Maintainers attest that access grants in production match this matrix.

Review outcomes are recorded in the pull request or issue that triggered the review.

## Change Log

| Date | Change | Author |
| --- | --- | --- |
| 2025-01-01 | Initial data access matrix. | Governance }
