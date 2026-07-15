# Contributing to Little Boy's Aegis

Thank you for helping improve Little Boy's Aegis. This project is open source, security-focused, and intentionally split across multiple repositories so each part can be reviewed and tested independently.

## Start in the right repository

Open issues and pull requests in the repository that owns the change:

| Area | Repository |
|---|---|
| Local orchestration, Docker, Kubernetes, Helm | `aegis-bank-deployment` |
| Banking API and security events | `aegis-bank-backend` |
| Banking web client | `aegis-bank-web-client` |
| Mobile app | `aegis-bank-mobile-app` |
| SOC dashboard | `dashboard` |
| SOAR engine, connectors, playbooks | `aegis-soar-engine` |
| Layer 1 detection agents | `agent-layer-1` |
| Layer 2 correlation and response decisions | `agent-layer-2` |
| Response simulation sandbox | `aegis-staging-sandbox` |
| AWS infrastructure | `aegis-bank-terraform` |

For cross-repository proposals, open a design issue in the repository with the largest expected implementation impact and link follow-up issues from there.

## What to include

- Explain the problem, expected behavior, and the repository area affected.
- Keep pull requests focused and small enough to review.
- Add or update tests when changing behavior.
- Update documentation when changing setup, APIs, schemas, policy gates, or operational assumptions.
- Never commit secrets, real customer data, cloud credentials, tokens, private keys, production logs, or exploit artifacts from systems you do not own.

## Security and safety expectations

Little Boy's Aegis includes attack simulation and vulnerable-mode demonstrations for defensive evaluation. Contributions must keep those capabilities safe:

- Run offensive scenarios only against systems you own or are explicitly authorized to test.
- Use synthetic data and local lab environments.
- Keep vulnerable modes isolated and clearly documented.
- Do not add persistence, evasion, credential theft, destructive payloads, or uncontrolled scanning.
- For response automation, document evidence requirements, authorization policy, blast-radius limits, audit fields, and rollback behavior.

## Pull request checklist

Before opening a pull request, confirm that:

- The change has a clear issue, motivation, or review note.
- Tests or validation steps are included in the pull request description.
- Security-sensitive behavior has a threat model note.
- Documentation reflects the new behavior.
- The contribution is compatible with the Apache License 2.0.

## License

Unless explicitly stated otherwise, contributions submitted to Little Boy's Aegis are provided under the Apache License 2.0.
