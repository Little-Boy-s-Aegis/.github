# Governance

Little Boy's Aegis is maintained by Team Little Boy and community contributors.

## Project goals

- Provide an open, inspectable AI-native cyber defense platform for banking-style simulations.
- Keep response automation explainable, policy-gated, reversible, and safe by default.
- Support defensive research, purple-team exercises, and security engineering education.

## Roles

| Role | Responsibility |
|---|---|
| Maintainers | Review and merge changes, set project direction, manage releases, and protect community standards. |
| Security reviewers | Review vulnerability reports, security-sensitive pull requests, response automation, policy changes, and hardening work. |
| Contributors | Improve code, documentation, tests, threat mappings, playbooks, deployment paths, and user experience. |

## Decision process

Routine changes can be accepted by maintainer review in the affected repository. Cross-repository architecture changes, public API changes, security policy changes, response automation changes, and license/governance changes should be discussed in an issue before implementation.

Security-sensitive decisions should include evidence requirements, risk tradeoffs, rollback plans, and auditability. When maintainers disagree, prefer the option that preserves user safety, least privilege, and reversible operation.

## Maintainer expectations

Maintainers should:

- review contributions with specific and actionable feedback;
- keep unsafe defaults out of the project;
- document major decisions in issues, pull requests, or README updates;
- disclose known limitations clearly;
- protect contributor safety and responsible security handling.
