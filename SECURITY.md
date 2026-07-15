# Security Policy

Little Boy's Aegis is a cybersecurity research, education, and simulation project. We welcome good-faith vulnerability reports and defensive hardening suggestions.

## Supported scope

Security reports may cover public repositories under the `Little-Boy-s-Aegis` organization, including the banking demo applications, SOC dashboard, SOAR engine, agent layers, deployment code, and Terraform reference architecture.

The project is not a certified banking product. Production deployments, cloud accounts, private infrastructure, and third-party systems are outside the scope of this policy unless their owner has given explicit written authorization.

## Reporting a vulnerability

Please do not open a public issue with exploit details.

Use GitHub private vulnerability reporting or a repository security advisory in the affected repository when available. If private reporting is not available, open a minimal public issue titled `Security contact request` without technical details, or contact a maintainer through an existing private channel.

Include as much of the following as you can safely share:

- affected repository, component, branch, version, or commit;
- impact and likely severity;
- concise reproduction steps using synthetic data;
- proof-of-concept details that do not expose real secrets or third-party systems;
- suggested mitigation, if known.

## Safe research rules

- Test only systems you own or are explicitly authorized to test.
- Do not access, modify, exfiltrate, or retain data that is not yours.
- Do not deploy persistence, malware, credential theft, destructive payloads, or uncontrolled scanning.
- Keep attack simulations inside local or authorized lab environments.
- Stop testing and report promptly if you encounter sensitive data or unintended exposure.

## Response expectations

Maintainers aim to acknowledge valid reports within 7 days and provide an initial triage response within 14 days. Timelines may vary because this is a community project, but we will prioritize issues that affect safe local operation, secret handling, authorization, response automation, or supply-chain integrity.

## Public disclosure

Please coordinate disclosure with maintainers. Public write-ups should wait until a fix, mitigation, or clear maintainer response is available, unless there is an overriding safety reason to disclose earlier.
