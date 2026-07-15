<div align="center">

# Little Boy's Aegis

### An AI-native cyber defense platform for modern banking

**1st Place Winner — [Shinhan Bank Future Lab's Track](https://futureslab.com.vn) (Financial Services) — [Agentic AI Build Week 2026](https://aabw.genaifund.ai)**

From customer transactions to the SOC: observe, correlate, verify, decide, and respond—without surrendering control.

[![1st Place](https://img.shields.io/badge/AABW_2026-1st_Place-FFD700?style=for-the-badge)](https://aabw.genaifund.ai)
[![Shinhan Bank Future Lab](https://img.shields.io/badge/Track-Shinhan_Bank_Future_Lab-0046FF?style=for-the-badge)](https://futureslab.com.vn)
[![Repositories](https://img.shields.io/badge/repositories-10-111827?style=for-the-badge&logo=github)](https://github.com/orgs/Little-Boy-s-Aegis/repositories)
[![MITRE ATT&CK](https://img.shields.io/badge/MITRE-ATT%26CK-E11D48?style=for-the-badge)](https://attack.mitre.org/)
[![CAPEC](https://img.shields.io/badge/knowledge-CAPEC-7C3AED?style=for-the-badge)](https://capec.mitre.org/)
[![Policy as Code](https://img.shields.io/badge/policy-OPA-14B8A6?style=for-the-badge&logo=openpolicyagent)](https://www.openpolicyagent.org/)

[Explore the platform](#the-platform) · [See the architecture](#how-aegis-works) · [Meet the team](#the-team) · [Repository map](#repository-map) · [Validation results](#validation-results) · [Run it locally](#run-the-ecosystem) · [Browse every repository](https://github.com/orgs/Little-Boy-s-Aegis/repositories)

</div>

---

## About the Hackathon

**Little Boy's Aegis** was built by **Team Little Boy** for the [Agentic AI Build Week (AABW) 2026](https://aabw.genaifund.ai) — Southeast Asia's largest on-site AI buildathon, organized by [GenAI Fund](https://genaifund.ai). The event brought together **2,000+ builders**, **10 enterprise partners**, and the full AI stack for five days in Ho Chi Minh City (July 8–12, 2026).

Our team competed in the **Financial Services I** track, sponsored by [Shinhan Future's Lab](https://futureslab.com.vn), where we built an AI-native SOC platform for banking cybersecurity — and **won 1st place** in the track. (Official results: [GenAI Fund LinkedIn](https://www.linkedin.com/posts/genai-fund_aabw2026-aabwxgaf-activity-7482359686189445120-FEhQ) · [Facebook](https://www.facebook.com/genaifund/posts/122236514156289079))

| Detail | Info |
|---|---|
| Event | [Agentic AI Build Week (AABW) 2026](https://aabw.genaifund.ai) |
| Organizer | [GenAI Fund](https://genaifund.ai) |
| Track | Financial Services I — [Shinhan Future's Lab](https://futureslab.com.vn) |
| Result | 1st Place |
| Location | Ho Chi Minh City, Vietnam |
| Date | July 8–12, 2026 |
| Submission Portal | [AABW Portal](https://aitalent.genaifund.ai/hackathon) |
| Devpost | [agentic-ai-build-week-2026.devpost.com](https://agentic-ai-build-week-2026.devpost.com/) |
| Official Results | [GenAI Fund — LinkedIn](https://www.linkedin.com/posts/genai-fund_aabw2026-aabwxgaf-activity-7482359686189445120-FEhQ) · [GenAI Fund — Facebook](https://www.facebook.com/genaifund/posts/122236514156289079) |
| Team Announcement | [Team Lead — LinkedIn](https://www.linkedin.com/feed/update/urn:li:activity:7482425857790124032/) |

---

## The Team

<table>
  <tr>
    <th>Member</th>
    <th>Role</th>
    <th>Key Contributions in Aegis</th>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/L1nkinPark"><b>h1eudayne</b></a>
    </td>
    <td>
      <b>Team Lead</b><br/>
      Full-Stack · System Design · System Architecture · DevOps · Cloud Engineer Lead
    </td>
    <td>
      Designed the end-to-end Aegis system architecture and drew all system design / AWS architecture diagrams. Built the SOAR decision engine, Layer 2 orchestrator correlation & verification logic, and the complete AWS Terraform infrastructure (hackathon & production profiles). Set up CI/CD pipelines, Docker Compose orchestration, Kubernetes/Helm manifests, and the Kafka event backbone. Led full-stack development across the SOC dashboard (Go + React), Spring Boot banking API, and integrated the multi-layer AI agent pipeline.
    </td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/teikv"><b>teikv</b></a>
    </td>
    <td>
      Supporting Developer · Pentest Support · Idea Presenter
    </td>
    <td>
      Contributed to frontend and backend development across the banking web portal and mobile app. Assisted in penetration testing campaigns covering OWASP Top 10 vulnerability demonstrations (SQLi, XSS, IDOR, parameter tampering). Presented the Aegis concept, threat model, and defensive philosophy to stakeholders and judges. Helped shape the platform's security narrative and user-facing documentation.
    </td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/an1dee3301"><b>an1dee</b></a>
    </td>
    <td>
      Supporting Developer · Pentest Support · Layer 2 Setup · Idea Presenter
    </td>
    <td>
      Contributed to codebase development and assisted in penetration testing exercises. Set up Proof of Concept (PoC) exploits, OPA policy rules, and automated playbooks for the Layer 2 orchestrator—including correlation rules, response workflows, and policy-gated containment logic. Collaborated on ideation sessions and helped articulate the Aegis defense-in-depth strategy during presentations.
    </td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/habachcp6"><b>bachcp6</b></a>
    </td>
    <td>
      <b>Core Architecture</b> · Security Assessment · Pentest Strategy
    </td>
    <td>
      <b>Core Architecture:</b> Designed and authored the complete Layer 1/Layer 2 agent architecture — including system prompts, CAPEC/ATT&amp;CK threat matrices, detection schemas, risk scoring models, and incident response playbooks.<br/>
      <b>Security Assessment:</b> Led comprehensive penetration testing initiatives across the platform to identify and remediate vulnerabilities, ensuring robust security.
    </td>
  </tr>
</table>

---

## Defense that reasons—and proves its work

Little Boy's Aegis is an end-to-end attack-and-defense environment built around a realistic digital banking system. Banking applications generate real operational telemetry. Specialist, read-only agents inspect that evidence. A second-layer orchestrator correlates and independently verifies findings before the SOAR engine can select a response.

The result is a security platform designed around three convictions:

- **Evidence before action.** Agent findings are signals, not verdicts. Layer 2 verifies them against clean logs and operational context.
- **Automation needs boundaries.** OPA policy, verification gates, scoped targets, approval modes, audit trails, and rollback data stand between a model decision and an environment-changing action.
- **Security should be observable.** Kafka event streams, structured schemas, a real-time SOC dashboard, and deterministic risk tables make the decision path inspectable.

### At a glance

| Capability | Aegis approach |
|---|---|
| Detection | Three read-only specialists examine network/EDR, web/API/UEBA, and ATM/IAM telemetry. |
| Threat mapping | Findings use offline MITRE ATT&CK, CAPEC, and CWE-derived defensive knowledge. |
| Correlation | Layer 2 joins findings only when concrete entities and evidence support the relationship. |
| Verification | Claims are checked against clean logs, database activity, security controls, and operational context. |
| Risk | Deterministic `0–10` scoring combines threat knowledge, asset criticality, evidence, and local context. |
| Response | Playbooks separate non-disruptive SOC actions from policy-gated containment. |
| Governance | OPA authorization, explicit approval modes, immutable audit events, rollback data, and manual-only controls. |
| Delivery | Local Docker, Kubernetes/Helm/Kustomize, and modular AWS Terraform profiles. |

## How Aegis works

### System Design — Full Platform Overview

> The complete Aegis system design showing all four major layers: **Ingestion** (log collection via Fluentd & Kafka), **Layer 1 Sensor Agents** (in-depth AI analysis), **Layer 2 Orchestrator** (context correlation, decision & automated execution with HA cluster), and **Reporting & Notification** (feedback loop with the SOC). Includes data stores, integrations, OPA guardrails, audit & compliance, and time-bound action examples.

<div align="center">
  <a href="01-system-design-aegis-ha.png">
    <img src="01-system-design-aegis-ha.png" alt="Aegis System Design — Full Platform Overview" width="100%"/>
  </a>
</div>

### The decision path

1. **Observe** — the banking API, gateway, applications, and infrastructure emit security telemetry.
2. **Detect** — three domain specialists inspect internal network/EDR, e-banking/API/WAF/UEBA, and ATM/IAM signals.
3. **Correlate** — Layer 2 groups findings by concrete entities, time, technique, and plausible attack sequence.
4. **Verify** — claims are checked independently against clean logs and context; unsupported findings are capped or withheld from containment.
5. **Decide** — deterministic ATT&CK/CAPEC risk data and policy rules produce a schema-valid decision and playbook plan.
6. **Respond** — non-disruptive actions can be raised immediately; containment requires every safety gate to pass and remains scoped, reversible, and auditable.

### Contracts between the layers

Aegis treats agent communication as an API, not an informal chat. That boundary makes every handoff testable and keeps authority in the correct layer.

| Boundary | Contract | Responsibility |
|---|---|---|
| Telemetry → Layer 1 | Clean routed events and domain context | Provide factual input without granting write access to the sensor. |
| Layer 1 → Layer 2 | `littleboy.soc.layer1.agent_finding.v4` | Report threat state, finding type, masked evidence, entities, ATT&CK/CAPEC mappings, and prompt-safety metadata. |
| Layer 2 → SOC/SOAR | `littleboy.soc.layer2.orchestrator_decision.v8` | Record correlation, independent verification, final risk, actions, approval modes, audit fields, limitations, and rollback requirements. |
| SOAR → control adapter | Validated action intent | Execute only the target, scope, duration, and connector operation authorized by policy. |

Layer 1 is deliberately unable to emit a final risk score, priority, response mode, playbook choice, containment decision, or operational attack instruction. Layer 2 must be able to explain which evidence changed the outcome and which limitations remain.

### Incident lifecycle

| State | Transition | Condition |
|---|---|---|
| `[*]` → `NEW` | Finding received | A new finding arrives from Layer 1. |
| `NEW` → `ANALYZED` | Schema valid and correlated | The finding passes schema validation and entity correlation. |
| `ANALYZED` → `MONITORED` | Evidence is weak or unconfirmed | Insufficient evidence to act; moved to active monitoring. |
| `ANALYZED` → `MITIGATED` | Non-disruptive response completed | SOC-safe actions (notify, enrich, ticket) are executed. |
| `ANALYZED` → `CONTAINED` | Every automation gate passes | All 10 containment gates clear; scoped action is taken. |
| `MONITORED` → `ANALYZED` | New evidence arrives | Re-evaluation when supporting evidence surfaces. |
| `MITIGATED` → `CLOSED` | Analyst review and evidence preserved | Human analyst confirms resolution. |
| `CONTAINED` → `CLOSED` | Verification and rollback window complete | Post-containment checks pass. |
| `CONTAINED` → `ROLLED_BACK` | Safety check or operator decision | Containment reversed due to issue or analyst override. |
| `ROLLED_BACK` → `CLOSED` | State restored and audit finalized | System restored and full audit trail recorded. |

Redis maintains live incident and playbook state, while the audit path records transitions and execution outcomes for the SOC. Correlation uses a short sliding window and concrete entity links—such as account, user, host, IP, session, request, transaction, or object ID—to reduce duplicate incidents without merging unrelated activity.

---

## AWS Architecture

Aegis provides two complete AWS architecture profiles—a **cost-optimized hackathon** deployment and a **production-grade enterprise** deployment—each with both logical and detailed views.

### Production Architecture — Enterprise Grade

#### Logical View

> High-level production architecture showing all platform layers on AWS: Ingestion (Kinesis/MSK), Layer 1 AI Sensor Agents, Layer 2 Meta Analyzer (Decision Engine), Layer 3 Orchestration & Automation, Reporting & Notification, High Availability Orchestrator Cluster, full data stores, audit & compliance, security & protection, and observability & monitoring.

<div align="center">
  <a href="03-aws-production-logical.jpg">
    <img src="03-aws-production-logical.jpg" alt="AWS Production Architecture — Logical View" width="100%"/>
  </a>
</div>

#### VPC Deep Dive

> Detailed VPC-level production architecture with Multi-AZ deployment across two Availability Zones. Shows public/private/security/data subnet segmentation, ECS clusters with auto-scaling groups, RDS Multi-AZ synchronous replication, OpenSearch cross-AZ replication, orchestration layer with heartbeat & leader election, and complete security & protection stack (WAF, Shield, GuardDuty, Security Hub, Config).

<div align="center">
  <a href="02-aws-production-vpc-deep-dive-official.png">
    <img src="02-aws-production-vpc-deep-dive-official.png" alt="AWS Production Architecture — VPC Deep Dive" width="100%"/>
  </a>
</div>

---

### Cost-Optimized Architecture — Hackathon

#### Logical View

> Simplified, serverless-first architecture designed for hackathon MVP: AWS Lambda preprocessing, S3 raw log storage, Bedrock & SageMaker for AI analysis, Step Functions for orchestration, and a lean stack with estimated monthly cost of **~$30–$80/month**. Easy to deploy in 1 day and extend to production.

<div align="center">
  <a href="05-aws-cost-optimized-logical.jpg">
    <img src="05-aws-cost-optimized-logical.jpg" alt="AWS Cost-Optimized Architecture — Logical View" width="100%"/>
  </a>
</div>

#### Deployment Architecture

> Cost-optimized deployment with single AZ, serverless-first (Firehose + Lambda), ECS Fargate with right-sizing, RDS Single AZ, and OpenSearch Serverless. Estimated monthly cost of **~$110–$250/month** for low traffic. Includes full CI/CD pipeline with GitHub Actions, ECR, and ECS Fargate deployment.

<div align="center">
  <a href="04-aws-cost-optimized-deployment.jpg">
    <img src="04-aws-cost-optimized-deployment.jpg" alt="AWS Cost-Optimized Deployment Architecture" width="100%"/>
  </a>
</div>

---

## The platform

### Security intelligence and automation

| Repository | What it does |
|---|---|
| [`agent-layer-1`](https://github.com/Little-Boy-s-Aegis/agent-layer-1) | Read-only specialist agents for EDR, WAF/UEBA, and ATM/IAM telemetry. Emits masked, schema-validated findings mapped to MITRE ATT&CK and CAPEC. |
| [`agent-layer-2`](https://github.com/Little-Boy-s-Aegis/agent-layer-2) | The orchestration contract: correlation, independent verification, deterministic risk scoring, banking-specific response rules, output schemas, and playbooks. |
| [`aegis-soar-engine`](https://github.com/Little-Boy-s-Aegis/aegis-soar-engine) | Executable Python decision engine with Kafka ingestion, Redis incident state, database verification, policy evaluation, safety gates, rollback, audit integrity, threat-intelligence enrichment, and response connectors. |
| [`aegis-staging-sandbox`](https://github.com/Little-Boy-s-Aegis/aegis-staging-sandbox) | Authenticated simulation APIs for reversible Fortinet, CrowdStrike, Entra ID, and AWS WAF response workflows. |
| [`dashboard`](https://github.com/Little-Boy-s-Aegis/dashboard) | Go and React SOC workspace for live security events, incidents, file-integrity monitoring, attack simulation, and AI-assisted investigation. |

### Banking applications and delivery

| Repository | What it does |
|---|---|
| [`aegis-bank-backend`](https://github.com/Little-Boy-s-Aegis/aegis-bank-backend) | Spring Boot core banking REST API with PostgreSQL persistence, JWT authentication, Kafka event production, and attack/defense controls. |
| [`aegis-bank-web-client`](https://github.com/Little-Boy-s-Aegis/aegis-bank-web-client) | Next.js banking portal for customer workflows and security-control demonstrations. |
| [`aegis-bank-mobile-app`](https://github.com/Little-Boy-s-Aegis/aegis-bank-mobile-app) | Dart/Flutter mobile banking experience connected to the Aegis API. |
| [`aegis-bank-deployment`](https://github.com/Little-Boy-s-Aegis/aegis-bank-deployment) | Complete local and Kubernetes orchestration: Docker Compose, Helm, Kustomize, Nginx, Kafka KRaft, Fluent Bit, OPA, Vault, Redis, Qdrant, and security tests. |
| [`aegis-bank-terraform`](https://github.com/Little-Boy-s-Aegis/aegis-bank-terraform) | Modular AWS infrastructure for cost-optimized hackathon and multi-AZ production profiles, including identity, encryption, observability, edge, data, and AI services. |

## What makes the system different

### Split trust between sensors and decisions

Layer 1 cannot assign final risk, choose playbooks, authorize containment, or execute actions. Its job is to report masked evidence in a strict JSON contract. Layer 2 owns correlation and verification, preventing one confident sensor—or one prompt injection—from becoming an operational decision.

### Policy-gated response

Environment-changing containment is off by default. It requires a confirmed threat, independent Layer 2 verification, sufficient evidence strength and risk, an OPA allow decision, autopilot enablement, an approved execution window, a verified target, and a scoped, time-bound action with rollback available.

Critical banking operations—including core banking, SWIFT, HSM, ATM switch, critical VLAN, and disaster-recovery isolation—are **manual-only**.

#### Auto-containment gate

Every environment-changing action must satisfy all of the following conditions:

| Gate | Why it exists |
|---|---|
| Threat confirmed | Prevents anomaly-only signals from changing the environment. |
| Layer 2 verification performed | Keeps the sensor that raised a finding from validating itself. |
| Verification supported or strong | Requires clean evidence to support the reported behavior. |
| Risk above the response floor | Reserves containment for materially dangerous incidents. |
| OPA allows the action | Applies policy-as-code outside model reasoning. |
| SOC autopilot enabled | Requires an explicit operational opt-in; the default is off. |
| Execution window open | Respects approved change periods and operating conditions. |
| Target entity verified | Blocks actions against inferred, ambiguous, or missing targets. |
| Action scoped, time-bound, and reversible | Limits blast radius and prevents permanent uncontrolled changes. |
| Rollback available | Ensures the platform can restore prior state. |

If any gate fails, Aegis can still preserve evidence, increase monitoring, create a hunt, open or update a ticket, notify the SOC, or queue a recommendation for approval. It cannot silently promote a suggestion into containment.

### Threat knowledge that works offline

The project carries structured MITRE ATT&CK and CAPEC knowledge, surface multipliers, edge-case matrices, and calibrated `0–10` scoring tables. Decisions remain explainable even when external threat-intelligence services are unavailable.

### A full proving ground

The banking API, customer clients, SOC dashboard, multi-broker Kafka backbone, log pipeline, policy engine, secret management, vector database, response sandbox, and test suites run as one ecosystem. This makes Aegis useful for purple-team exercises, defensive AI research, playbook validation, and security engineering demonstrations.

## Defense in depth

| Layer | Controls |
|---|---|
| Edge | Nginx reverse proxy, request routing, security headers, CORS rules, cache controls, and gateway logging. |
| Identity | JWT validation, SOC session controls, CSRF protection, role boundaries, and simulated Entra ID actions. |
| Application | Banking authorization checks, structured validation, security-event production, and attack/defense toggles. |
| Data | PostgreSQL verification records, Redis workflow state, Qdrant defensive context, and Vault-backed secret workflows. |
| Event backbone | Three-node Kafka KRaft cluster, replicated streams, provisioned topics, malformed-event handling, and trusted/untrusted event separation. |
| Detection | Domain-specific Layer 1 agents, prompt-injection indicators, masked evidence, and schema enforcement. |
| Decision | Independent verification, entity correlation, deterministic risk tables, OPA policy, approval modes, and response floors. |
| Response | Connector isolation, rate limits, allowlists, dry-run support, rollback, audit-integrity checks, and staging simulation. |
| Delivery | Container security checks, CI security audits, Kubernetes policies, encrypted cloud resources, and infrastructure observability. |

## Event and response ecosystem

The deployment provides a high-availability Kafka backbone for banking events, gateway and application logs, normalized Layer 1 findings, fast-path detections, orchestrator decisions, and SOC updates. Fluent Bit collects container and gateway logs; the log parser normalizes and routes events to the appropriate specialist; Kafka decouples collection from analysis so the SOC remains observable during individual service restarts.

The SOAR engine supports a connector-oriented response model. Current adapters and simulations cover:

- network and edge response through Fortinet and WAF controls;
- endpoint isolation and reconnection through CrowdStrike-style workflows;
- identity response through Active Directory and Entra ID-style actions;
- intelligence enrichment through AbuseIPDB, Shodan, and VirusTotal connectors;
- notifications and case routing through email, Jira, PagerDuty, Telegram, webhooks, and MQTT;
- safe local exercises through the authenticated staging sandbox.

Connector availability does not imply permission to act. Each action still passes schema validation, policy evaluation, target validation, safety checks, execution controls, and audit recording.

## Technology map

| Area | Technologies |
|---|---|
| Experiences | Next.js, React, TypeScript, Flutter, Dart |
| Banking services | Java, Spring Boot, Hibernate/JPA, PostgreSQL |
| SOC and orchestration | Go, Python, Redis, Qdrant |
| Event and log pipeline | Apache Kafka KRaft, Fluent Bit |
| Security controls | Open Policy Agent, Vault, Nginx, JWT, audit/FIM controls |
| Platform engineering | Docker Compose, Kubernetes, Helm, Kustomize, Terraform, GitHub Actions |
| Threat knowledge | MITRE ATT&CK, CAPEC, CWE, deterministic risk calibration |

## Repository map

Little Boy's Aegis is split into focused repositories so each layer can be reviewed, tested, and deployed independently while still running as one local ecosystem.

| Repository | Purpose | Primary stack |
|---|---|---|
| [`aegis-bank-deployment`](https://github.com/Little-Boy-s-Aegis/aegis-bank-deployment) | Local platform orchestration, Nginx gateway, Kafka, OPA, Vault, Kubernetes manifests, and Helm chart. | Docker Compose, Nginx, Kafka, OPA, Vault, Kubernetes, Helm |
| [`aegis-bank-backend`](https://github.com/Little-Boy-s-Aegis/aegis-bank-backend) | Mock banking API, authentication, accounts, transfers, security toggles, and security-event publishing. | Java, Spring Boot, JPA/Hibernate, PostgreSQL/H2 |
| [`aegis-bank-web-client`](https://github.com/Little-Boy-s-Aegis/aegis-bank-web-client) | Customer-facing web banking portal for login, dashboard, transfer, transaction history, and security controls. | Next.js, React, TypeScript |
| [`aegis-bank-mobile-app`](https://github.com/Little-Boy-s-Aegis/aegis-bank-mobile-app) | Mobile banking client with offline demo mode and API-backed account/transfer flows. | Flutter, Dart |
| [`dashboard`](https://github.com/Little-Boy-s-Aegis/dashboard) | SOC dashboard, incident workbench, response center, log explorer, agent management, and backend APIs. | Go, React, TypeScript |
| [`aegis-soar-engine`](https://github.com/Little-Boy-s-Aegis/aegis-soar-engine) | SOAR decision engine, policy evaluation, playbook execution, connectors, audit logging, rollback, and safety gates. | Python, Redis, Qdrant |
| [`agent-layer-1`](https://github.com/Little-Boy-s-Aegis/agent-layer-1) | Read-only specialist sensor agents for internal network/EDR, e-banking/API/WAF/UEBA, and ATM/IAM domains. | Python, structured JSON contracts |
| [`agent-layer-2`](https://github.com/Little-Boy-s-Aegis/agent-layer-2) | Meta analyzer for entity correlation, independent verification, risk scoring, response selection, and schema-valid decisions. | Python, MITRE ATT&CK, CAPEC |
| [`aegis-staging-sandbox`](https://github.com/Little-Boy-s-Aegis/aegis-staging-sandbox) | Safe target environment for response simulation and connector validation before touching real controls. | Python, Flask |
| [`aegis-bank-terraform`](https://github.com/Little-Boy-s-Aegis/aegis-bank-terraform) | AWS hackathon and production-reference infrastructure profiles. | Terraform, AWS |

## Deployment choices

| Mode | Best for | Included approach |
|---|---|---|
| Local Compose | Demos, development, and purple-team labs | One-command multi-service environment behind the Nginx gateway. |
| Kubernetes local overlay | Cluster validation and platform engineering | Kustomize base plus local patches for the complete control and data plane. |
| Helm | Configurable packaged deployment | Aegis platform chart with service, policy, data-store, and secret configuration. |
| AWS hackathon profile | Cost-conscious cloud demonstrations | Serverless-first and single-AZ choices where appropriate. |
| AWS production profile | Architecture study and hardened adaptation | Multi-AZ networking, separated tiers, encryption, audit, observability, and edge controls. |

The production Terraform profile is an architectural starting point, not a certification. Organizations must apply their own threat model, data residency rules, banking regulations, identity model, key-management policy, disaster-recovery objectives, and change controls.

## Validation results

Aegis is validated as a security engineering system, not only as a set of services that boot. Public tests cover local behavior and safety contracts; a separate July 2026 source-assisted web/API plus AWS read-only posture review was used to triage hardening work without publishing sensitive evidence in this profile README.

| Validation area | What was checked | Result and status |
|---|---|---|
| Local 100-case adversarial run | Authentication, authorization, JWT handling, input validation, XSS probes, HTTP method handling, malformed requests, SSRF-style probes, resilience, and gateway behavior against `localhost`. | Produced a dev-facing hardening backlog: 43 pass, 4 warn, 53 fail. Most failures were controlled by gateway/API routing instability (`502`) rather than confirmed exploit paths, so the recommended next step is to stabilize routing and rerun authenticated checks. |
| SOAR and policy safety | Policy evaluation, playbook routing, action-worker dry runs, rollback behavior, rate limits, connector boundaries, secret handling, notifications, and audit integrity. | Covered by focused unit tests and safety checks in the SOAR engine. These tests support the core claim that response automation must pass policy, scope, execution, and audit gates. |
| SOC dashboard behavior | Login flow, response center workflows, dashboard workbench interactions, and frontend component behavior. | Covered by React/Vitest-style component tests and Go backend handler tests. |
| Load and ingestion baseline | Dashboard read load, SOAR ingestion stress, mixed read/write storms, and baseline latency scenarios. | k6 scenarios and result artifacts exist for local performance validation. These are baseline engineering checks, not production capacity claims. |
| Source and IaC review | Banking web/API source, SOC source, deployment config, Terraform profiles, cloud logging/detection posture, IAM/network posture, and AWS K8s/AD discovery across enabled regions. | 24 findings were triaged into a hardening backlog. The AWS K8s/AD evidence audit recorded 9/9 true positives and 0 false positives for that review set. |
| Negative evidence from cloud review | EKS/Kubernetes objects, AWS Directory Service, Managed AD, AD Connector, EC2 Windows/domain-controller candidates, public AD ports, and public Kubernetes control-plane ports. | No live EKS/AD objects or public K8s/AD control-plane exposure were identified in the reviewed AWS regions. Source/IaC review also did not find active EKS or AWS Directory Service definitions. |

The combined security review intentionally separates confirmed evidence from assumptions. Items such as secret handling, lab-only vulnerable modes, transport configuration, IAM scoping, detection coverage, and default-network hygiene are treated as hardening backlog unless a retest proves closure.

Known coverage gaps remain: active authenticated browser/DAST testing, two-user authorization boundary tests, container image scanning, Prowler/ScoutSuite-style cloud posture scans, and deeper per-principal IAM analysis should be run before any production adaptation.

## Run the ecosystem

Little Boy's Aegis is a **microservice architecture** spread across multiple repositories. The `docker-compose.yml` in `aegis-bank-deployment` builds each service from sibling directories using relative paths (`../BE`, `../FE_Web`, `../dashboard`, `../soar-engine`, etc.). This means **all repos must be cloned into specific directory names in the same parent folder**.

### Prerequisites

| Requirement | Minimum version | Purpose |
|---|---|---|
| [Git](https://git-scm.com/) | 2.30+ | Clone all repositories |
| [WSL 2](https://learn.microsoft.com/windows/wsl/install) | Windows only | Linux backend used by Docker Desktop |
| [Docker Desktop](https://docs.docker.com/get-docker/) | 24.0+ | Container runtime + Compose V2 with WSL 2 backend |
| RAM | **8 GB minimum** (16 GB recommended) | 3-node Kafka cluster + AI agents + databases |
| Disk | 10 GB+ free | Docker images, volumes, and build cache |

### Step 0 -- Install Docker, WSL, and Git

If you already have **Git**, **Docker Desktop**, and **WSL 2** working, skip to Step 1.

#### Windows 10/11 setup

Use **PowerShell** for the project commands in this README. WSL is required because Docker Desktop uses it internally, but you do not need to run the project from the Ubuntu terminal.

1. Open **PowerShell as Administrator**:

```powershell
wsl --install -d Ubuntu
```

Restart your computer if Windows asks. After restart, open **Ubuntu** once from the Start menu and create a username/password if prompted.

If WSL was already installed before, run:

```powershell
wsl --update
wsl --set-default-version 2
```

2. Install **Git for Windows**:

Download and install Git from [git-scm.com](https://git-scm.com/download/win). The default installer options are fine.

3. Install **Docker Desktop**:

Download and install Docker Desktop from [docs.docker.com/get-docker](https://docs.docker.com/get-docker/). During setup, keep **Use WSL 2 instead of Hyper-V** enabled if the installer shows it.

4. Start Docker Desktop:

Open Docker Desktop and wait until it says **Docker Desktop is running**. Then check these settings:

| Docker Desktop setting | Value |
|---|---|
| Settings -> General | Enable **Use the WSL 2 based engine** |
| Settings -> Resources -> WSL Integration | Enable integration for **Ubuntu** |
| Settings -> Resources -> Advanced | Give Docker at least **8 GB memory** if your machine has enough RAM |

5. Verify everything:

```powershell
wsl --list --verbose
git --version
docker --version
docker compose version
docker run hello-world
```

Expected result:

- `wsl --list --verbose` shows Ubuntu with `VERSION 2`.
- `git --version` prints a Git version.
- `docker compose version` prints a Compose V2 version.
- `docker run hello-world` downloads a small test image and exits successfully.

#### macOS setup

Install [Git](https://git-scm.com/download/mac) and [Docker Desktop for Mac](https://docs.docker.com/get-docker/), then open Docker Desktop and wait until it is running.

Verify:

```bash
git --version
docker --version
docker compose version
docker run hello-world
```

#### Linux setup

Install Git, Docker Engine, and Docker Compose Plugin using your distro package manager. On Ubuntu:

```bash
sudo apt update
sudo apt install -y git ca-certificates curl
curl -fsSL https://get.docker.com | sudo sh
sudo usermod -aG docker "$USER"
newgrp docker
docker compose version
docker run hello-world
```

### Step 1 -- Clone all repositories

> [!IMPORTANT]
> The `docker-compose.yml` uses **specific directory names** (`../BE`, `../FE_Web`, `../soar-engine`, etc.) that differ from the GitHub repo names. You **must** clone into the exact directory names shown below, or Docker Compose will fail with "path not found" errors.

**Linux / macOS:**

```bash
mkdir -p aegis-workspace && cd aegis-workspace

# Clone with correct directory names (matching docker-compose.yml paths)
git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-deployment.git
git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-backend.git       BE
git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-web-client.git     FE_Web
git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-mobile-app.git     FE_App
git clone https://github.com/Little-Boy-s-Aegis/aegis-soar-engine.git         soar-engine
git clone https://github.com/Little-Boy-s-Aegis/aegis-staging-sandbox.git     staging-sandbox
git clone https://github.com/Little-Boy-s-Aegis/dashboard.git
git clone https://github.com/Little-Boy-s-Aegis/agent-layer-1.git
git clone https://github.com/Little-Boy-s-Aegis/agent-layer-2.git
```

**Windows (PowerShell):**

```powershell
mkdir aegis-workspace; cd aegis-workspace

git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-deployment.git
git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-backend.git       BE
git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-web-client.git     FE_Web
git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-mobile-app.git     FE_App
git clone https://github.com/Little-Boy-s-Aegis/aegis-soar-engine.git         soar-engine
git clone https://github.com/Little-Boy-s-Aegis/aegis-staging-sandbox.git     staging-sandbox
git clone https://github.com/Little-Boy-s-Aegis/dashboard.git
git clone https://github.com/Little-Boy-s-Aegis/agent-layer-1.git
git clone https://github.com/Little-Boy-s-Aegis/agent-layer-2.git
```

After cloning, your directory **must** look exactly like this:

```
aegis-workspace/                       <-- you are here
  aegis-bank-deployment/               <-- Docker Compose, Nginx, Kafka, OPA, Vault
  BE/                                  <-- Spring Boot banking REST API (Java)
  FE_Web/                              <-- Next.js banking portal (TypeScript/React)
  FE_App/                              <-- Flutter mobile banking app (Dart)
  soar-engine/                         <-- SOAR decision engine + action workers (Python)
  staging-sandbox/                     <-- Staging simulation APIs
  dashboard/                           <-- SOC Dashboard: Go backend + React frontend
  agent-layer-1/                       <-- AI Sensor Agents: EDR, WAF/UEBA, ATM/IAM (Python)
  agent-layer-2/                       <-- Meta Analyzer: correlation, risk scoring (Python)
```

> [!NOTE]
> `aegis-bank-terraform` is only needed for AWS cloud deployment, not for running locally.

### Step 2 -- Configure and start

Make sure **Docker Desktop is running** before this step.

**Linux / macOS:**

```bash
cd aegis-bank-deployment

# Copy environment template -- all defaults work for local dev
cp .env.example .env
```

**Windows (PowerShell):**

```powershell
cd aegis-bank-deployment

# Copy environment template -- all defaults work for local dev
Copy-Item .env.example .env

# Open the file in Notepad
notepad .env
```

**The only required edit** is your AI provider API key. Open `.env` and set **one** of these:

```bash
# Option A: AWS Bedrock with Qwen (used in hackathon, default in .env.example)
LLM_PROVIDER=bedrock
BEDROCK_MODEL_ID=qwen.qwen3-coder-next
BEDROCK_REGION=ap-southeast-2

# Option B: OpenAI
# LLM_PROVIDER=openai
# OPENAI_API_KEY=sk-your-actual-api-key-here

# Option C: Qwen direct
# LLM_PROVIDER=qwen
# QWEN_API_KEY=your-qwen-api-key
```

Everything else (database passwords, JWT secrets, Kafka config, ports) **already has working defaults** for local development. No further edits needed.

Now build and start:

```bash
# Build and start all 22 containers
docker compose up --build -d
```

> [!WARNING]
> The **first build takes 10--15 minutes** as Docker compiles Java (Spring Boot), Go (SOC backend), Python (AI agents, SOAR engine), and Node.js (Next.js, React) projects from source. Subsequent starts are much faster since images are cached.

Services start in dependency order: **PostgreSQL, Redis, Qdrant** --> **Kafka cluster** (~30s for KRaft leader election) --> **backends** --> **AI agents and SOAR** --> **frontends** --> **Nginx gateway**.

### Step 3 -- Access the platform

Once all containers are healthy (`docker compose ps`), open your browser:

| Service | URL | Description |
|---|---|---|
| Banking Portal | [`http://localhost/`](http://localhost/) | Next.js customer-facing banking application |
| SOC Dashboard | [`http://localhost/soc/`](http://localhost/soc/) | Security Operations Center workspace |
| Banking API | [`http://localhost/api-bank/`](http://localhost/api-bank/) | Spring Boot REST API (strips prefix, proxies to backend) |
| SOC Backend API | [`http://localhost/api/`](http://localhost/api/) | Go SOC backend API |
| Kafdrop (Kafka UI) | [`http://localhost:9000/`](http://localhost:9000/) | Kafka topic browser (protected by HTTP Basic Auth) |

All traffic on port 80 goes through **Nginx** which routes to internal services. Kafdrop runs on a **separate port 9000** with HTTP Basic Auth.

#### Banking portal login

Open [`http://localhost/login`](http://localhost/login) (or open [`http://localhost/`](http://localhost/) and let it redirect), then use one of the seeded demo accounts:

| User | Username | Password | Use for |
|---|---|---|---|
| Alice Smith | `alice` | `password123` | Customer dashboard, transfers, transaction history, attack/defense demos |
| Bob Jones | `bob` | `password123` | Second customer account for transfer, IDOR/BOLA, and stored-XSS scenarios |
| Administrator | `admin` | `admin123` | Admin/security-control workflows |

#### SOC dashboard login

Open [`http://localhost/soc/`](http://localhost/soc/). The SOC uses a two-step operator login:

1. Enter operator UID `10001`.
2. Click **Request Login Token**.
3. Read the generated SHA-256 token from the SOC backend container:

```bash
docker exec aegis-dashboard-backend cat /tmp/otp.txt
```

If you are running an older image that writes the OTP file in the container working directory, use:

```bash
docker exec aegis-dashboard-backend cat otp.txt
```

4. Copy the token after `-->`, paste it into the SOC login form, then click **Verify & Login**.

The SOC token is generated on demand, expires after a short window, and is consumed after a successful login.

### What starts locally (22 containers)

| Layer | Services | Internal ports |
|---|---|---|
| **Gateway** | Nginx reverse proxy (port 80 + 9000) | 80, 9000 |
| **Frontend** | Banking portal (Next.js), SOC dashboard (React) | 3000, 3001 |
| **Backend** | Banking API (Spring Boot), SOC backend (Go) | 8080, 8082 |
| **AI and SOAR** | SOAR orchestrator (active + standby), action workers (active + standby), vector DB init | 8092 |
| **Data** | PostgreSQL 16, Redis 7, Qdrant (vector DB) | 5432, 6379, 6333 |
| **Event Backbone** | 3-node Kafka KRaft cluster, Kafdrop UI, Fluent Bit, log parser, Kafka topic init | 9092--9094, 9000, 24224, 8088 |
| **Security** | OPA, Vault (dev mode), Vault init | 8181, 8200 |
| **Staging** | Staging sandbox (response simulation) | 8095 |

### Useful commands

```bash
# Follow all platform logs
docker compose logs -f

# Watch specific layers
docker compose logs -f kafka-1 kafka-2 kafka-3 fluent-bit log-parser     # Event pipeline
docker compose logs -f soar-orchestrator soar-action-worker               # SOAR engine
docker compose logs -f be-backend fe-web                                  # Banking apps
docker compose logs -f dashboard-backend dashboard-frontend               # SOC Dashboard

# Check service health
docker compose ps

# Restart a specific service
docker compose restart soar-orchestrator

# Stop services (keep data volumes)
docker compose down

# Full reset -- delete all volumes and rebuild from scratch
docker compose down -v && docker compose up --build -d
```

### Troubleshooting

| Issue | Solution |
|---|---|
| `path "../BE" not found` or similar | Clone repos with the **exact directory names** shown in Step 1. The docker-compose.yml expects `../BE`, not `../aegis-bank-backend`. |
| Containers keep restarting | Run `docker compose logs <service>` to check errors. |
| `docker` command not found | Install Docker Desktop, reopen PowerShell/Terminal, then run `docker --version`. |
| `Cannot connect to the Docker daemon` | Open Docker Desktop and wait until it says **Docker Desktop is running**. |
| `docker compose` is not recognized | Update Docker Desktop. Use `docker compose`, not the older `docker-compose`. |
| WSL shows `VERSION 1` | Run `wsl --set-default-version 2`, then restart Docker Desktop. |
| Docker Desktop WSL error | Run `wsl --update`, reboot Windows, then start Docker Desktop again. |
| Kafka not ready | KRaft cluster needs ~30s to elect a leader. Check `docker compose logs kafka-1`. |
| AI/SOAR agents return errors | Verify your LLM provider and API credentials in `.env`. |
| Out of memory / Docker crashes | Increase Docker Desktop memory to **8 GB+** in Settings --> Resources. |
| Port 80 already in use | Change `NGINX_PORT` in `.env` or stop the conflicting service. |
| First build takes forever | Normal -- compiling 4 languages from source takes 10--15 min on first run. |

### Kubernetes and AWS deployment

For Kubernetes-based deployment, `aegis-bank-deployment` also includes Helm charts and Kustomize overlays:

```bash
# Kustomize (local overlay)
kubectl apply -k aegis-bank-deployment/kubernetes/overlays/local

# Helm
helm install aegis aegis-bank-deployment/helm/aegis-platform -f values-local.yaml
```

For AWS cloud deployment, clone and use [`aegis-bank-terraform`](https://github.com/Little-Boy-s-Aegis/aegis-bank-terraform):

```bash
git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-terraform.git terraform
cd terraform
terraform init && terraform apply -var-file=environments/hackathon/terraform.tfvars    # ~$30-80/month
```

> [!WARNING]
> The production Terraform profile is an architectural starting point, not a certification. Apply your own threat model, data residency rules, and banking regulations before deploying to production.

## Validation philosophy

Aegis uses multiple validation layers because passing unit tests alone does not prove that a security control works across service boundaries.

- **Contract tests** validate Layer 1 and Layer 2 JSON schemas and required safety fields.
- **Unit tests** cover policy evaluation, playbook routing, rollback, rate limiting, secret handling, notifications, and audit integrity.
- **Integration tests** exercise Kafka, Redis, PostgreSQL verification, the staging sandbox, and connector behavior.
- **Platform tests** inspect container security, frontend protections, prompt behavior, and SOAR controls.
- **Adversarial suites** probe authentication, authorization, JWT handling, injection, XSS, event forgery, resilience, exposed services, secrets, and gateway behavior while preserving evidence per case.
- **CI security checks** provide repeatable repository-level quality gates; environment-specific results remain separate from this organization profile.

Security findings are not hidden behind a marketing badge. A failed check represents a control or configuration to investigate, while a blocked check means coverage was incomplete—not that the target passed.

## Start where you work

| If you are a… | Begin with… | You can contribute… |
|---|---|---|
| Detection engineer | [`agent-layer-1`](https://github.com/Little-Boy-s-Aegis/agent-layer-1) | Telemetry mappings, masked evidence rules, ATT&CK/CAPEC coverage, and prompt-safety tests. |
| SOC analyst | [`dashboard`](https://github.com/Little-Boy-s-Aegis/dashboard) | Incident workflows, investigation views, triage ergonomics, reporting, and analyst feedback loops. |
| SOAR engineer | [`aegis-soar-engine`](https://github.com/Little-Boy-s-Aegis/aegis-soar-engine) | Verification sources, playbooks, connectors, safety gates, rollback, and auditability. |
| Application security engineer | [`aegis-bank-backend`](https://github.com/Little-Boy-s-Aegis/aegis-bank-backend) | Banking abuse cases, authorization controls, secure events, and defensive test coverage. |
| Platform engineer | [`aegis-bank-deployment`](https://github.com/Little-Boy-s-Aegis/aegis-bank-deployment) | Kubernetes, Helm, policy, secrets, observability, resilience, and supply-chain controls. |
| Cloud architect | [`aegis-bank-terraform`](https://github.com/Little-Boy-s-Aegis/aegis-bank-terraform) | AWS landing-zone design, IAM, encryption, networking, cost controls, and reliability. |
| AI safety researcher | [`agent-layer-2`](https://github.com/Little-Boy-s-Aegis/agent-layer-2) | Trust boundaries, structured decisions, verification caps, prompt-injection resistance, and evaluation cases. |

## Built for safe experimentation

Little Boy's Aegis is a research, education, and security-simulation project—not a certified banking product or a substitute for production security controls. Run offensive scenarios only in systems you own or are explicitly authorized to test. Validate policies, secrets, network boundaries, connectors, and rollback behavior before adapting any component to a real environment.

The project intentionally includes attack simulation and configurable vulnerable behaviors for defensive evaluation. Keep those modes isolated, use synthetic data, rotate every example credential, and never connect a lab control adapter to production infrastructure.

## Explore and contribute

Start with [`aegis-bank-deployment`](https://github.com/Little-Boy-s-Aegis/aegis-bank-deployment) to experience the complete system, or enter through the repository that matches your craft:

- Detection engineering: [`agent-layer-1`](https://github.com/Little-Boy-s-Aegis/agent-layer-1)
- Decision contracts and playbooks: [`agent-layer-2`](https://github.com/Little-Boy-s-Aegis/agent-layer-2)
- SOAR and integrations: [`aegis-soar-engine`](https://github.com/Little-Boy-s-Aegis/aegis-soar-engine)
- SOC experience: [`dashboard`](https://github.com/Little-Boy-s-Aegis/dashboard)
- Platform engineering: [`aegis-bank-deployment`](https://github.com/Little-Boy-s-Aegis/aegis-bank-deployment) and [`aegis-bank-terraform`](https://github.com/Little-Boy-s-Aegis/aegis-bank-terraform)

Open an issue or pull request in the repository you want to improve. When proposing response automation, include its evidence requirements, authorization policy, blast-radius limit, audit fields, and rollback path.

---

<div align="center">

**Little Boy's Aegis — 1st Place, [Shinhan Bank Future Lab's Track](https://futureslab.com.vn) (Financial Services), [AABW 2026](https://aabw.genaifund.ai)**

**Intelligence at machine speed, control at human depth.**

[All repositories](https://github.com/orgs/Little-Boy-s-Aegis/repositories) | [AABW Event](https://aabw.genaifund.ai) | [GenAI Fund](https://genaifund.ai) | [Shinhan Future's Lab](https://futureslab.com.vn)

</div>
