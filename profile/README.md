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

[Explore the platform](#the-platform) · [See the architecture](#how-aegis-works) · [Meet the team](#the-team) · [Run it locally](#run-the-ecosystem) · [Browse every repository](https://github.com/orgs/Little-Boy-s-Aegis/repositories)

</div>

---

## About the Hackathon

**Little Boy's Aegis** was built by **Team Little Boy** for the [Agentic AI Build Week (AABW) 2026](https://aabw.genaifund.ai) — Southeast Asia's largest on-site AI buildathon, organized by [GenAI Fund](https://genaifund.ai). The event brought together **2,000+ builders**, **10 enterprise partners**, and the full AI stack for five days in Ho Chi Minh City (July 8–12, 2026).

Our team competed in the **Financial Services I** track, sponsored by [Shinhan Future's Lab](https://futureslab.com.vn), where we built an AI-native SOC platform for banking cybersecurity — and **won 1st place** in the track. ([Winning announcement on LinkedIn](https://www.linkedin.com/feed/update/urn:li:activity:7482425857790124032/))

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
| Announcement | [LinkedIn Post](https://www.linkedin.com/feed/update/urn:li:activity:7482425857790124032/) |

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
      <b>Lead Pentester</b> · Core Architecture · Pentest Strategy
    </td>
    <td>
      Core Architecture: Engineered and developed the foundational Layer 1 and Layer 2 (L1/L2) infrastructure for the agent system. Security Assessment: Executed comprehensive penetration testing across the platform to identify and remediate vulnerabilities, ensuring robust security.
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
  <img src="01-system-design.png" alt="Aegis System Design — Full Platform Overview" width="100%"/>
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
  <img src="03-aws-production-logical.jpg" alt="AWS Production Architecture — Logical View" width="100%"/>
</div>

#### VPC Deep Dive

> Detailed VPC-level production architecture with Multi-AZ deployment across two Availability Zones. Shows public/private/security/data subnet segmentation, ECS clusters with auto-scaling groups, RDS Multi-AZ synchronous replication, OpenSearch cross-AZ replication, orchestration layer with heartbeat & leader election, and complete security & protection stack (WAF, Shield, GuardDuty, Security Hub, Config).

<div align="center">
  <img src="02-aws-production-vpc-deep-dive.jpg" alt="AWS Production Architecture — VPC Deep Dive" width="100%"/>
</div>

---

### Cost-Optimized Architecture — Hackathon

#### Logical View

> Simplified, serverless-first architecture designed for hackathon MVP: AWS Lambda preprocessing, S3 raw log storage, Bedrock & SageMaker for AI analysis, Step Functions for orchestration, and a lean stack with estimated monthly cost of **~$30–$80/month**. Easy to deploy in 1 day and extend to production.

<div align="center">
  <img src="05-aws-cost-optimized-logical.jpg" alt="AWS Cost-Optimized Architecture — Logical View" width="100%"/>
</div>

#### Deployment Architecture

> Cost-optimized deployment with single AZ, serverless-first (Firehose + Lambda), ECS Fargate with right-sizing, RDS Single AZ, and OpenSearch Serverless. Estimated monthly cost of **~$110–$250/month** for low traffic. Includes full CI/CD pipeline with GitHub Actions, ECR, and ECS Fargate deployment.

<div align="center">
  <img src="04-aws-cost-optimized-deployment.jpg" alt="AWS Cost-Optimized Deployment Architecture" width="100%"/>
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

## Deployment choices

| Mode | Best for | Included approach |
|---|---|---|
| Local Compose | Demos, development, and purple-team labs | One-command multi-service environment behind the Nginx gateway. |
| Kubernetes local overlay | Cluster validation and platform engineering | Kustomize base plus local patches for the complete control and data plane. |
| Helm | Configurable packaged deployment | Aegis platform chart with service, policy, data-store, and secret configuration. |
| AWS hackathon profile | Cost-conscious cloud demonstrations | Serverless-first and single-AZ choices where appropriate. |
| AWS production profile | Architecture study and hardened adaptation | Multi-AZ networking, separated tiers, encryption, audit, observability, and edge controls. |

The production Terraform profile is an architectural starting point, not a certification. Organizations must apply their own threat model, data residency rules, banking regulations, identity model, key-management policy, disaster-recovery objectives, and change controls.

## Run the ecosystem

Little Boy's Aegis is a **microservice architecture** with 10 repositories. This section walks you through cloning everything, setting up prerequisites, and running the full platform locally.

### Prerequisites

| Requirement | Minimum version | Purpose |
|---|---|---|
| [Git](https://git-scm.com/) | 2.30+ | Clone all repositories |
| [Docker](https://docs.docker.com/get-docker/) | 24.0+ | Container runtime |
| [Docker Compose](https://docs.docker.com/compose/) | 2.20+ (V2) | Multi-service orchestration |
| RAM | 8 GB+ (16 GB recommended) | Kafka cluster + AI agents + databases |
| Disk | 10 GB+ free | Images, volumes, and build cache |

Optional: [Node.js](https://nodejs.org/) 18+ (for frontend dev), [Go](https://go.dev/) 1.21+ (for SOC backend dev), [Java](https://adoptium.net/) 17+ (for banking API dev), [Flutter](https://flutter.dev/) 3.x (for mobile app dev).

### Step 1 — Clone all repositories

Run the following script to clone every repository into a single workspace directory:

```bash
# Create workspace and clone all repos
mkdir -p aegis-workspace && cd aegis-workspace

# Core platform
git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-deployment.git
git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-backend.git
git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-web-client.git
git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-mobile-app.git

# AI & Security layers
git clone https://github.com/Little-Boy-s-Aegis/agent-layer-1.git
git clone https://github.com/Little-Boy-s-Aegis/agent-layer-2.git
git clone https://github.com/Little-Boy-s-Aegis/aegis-soar-engine.git
git clone https://github.com/Little-Boy-s-Aegis/aegis-staging-sandbox.git

# SOC Dashboard
git clone https://github.com/Little-Boy-s-Aegis/dashboard.git

# Infrastructure as Code
git clone https://github.com/Little-Boy-s-Aegis/aegis-bank-terraform.git
```

Or clone everything in one command:

```bash
mkdir -p aegis-workspace && cd aegis-workspace && \
for repo in aegis-bank-deployment aegis-bank-backend aegis-bank-web-client aegis-bank-mobile-app agent-layer-1 agent-layer-2 aegis-soar-engine aegis-staging-sandbox dashboard aegis-bank-terraform; do \
  git clone https://github.com/Little-Boy-s-Aegis/$repo.git; \
done
```

### Repository map

After cloning, your workspace will look like this:

```
aegis-workspace/
  aegis-bank-deployment/     # Docker Compose, Helm, Kustomize, Nginx, Kafka, OPA, Vault
  aegis-bank-backend/        # Spring Boot core banking REST API (Java)
  aegis-bank-web-client/     # Next.js banking portal (TypeScript/React)
  aegis-bank-mobile-app/     # Flutter mobile banking app (Dart)
  agent-layer-1/             # AI Sensor Agents — EDR, WAF/UEBA, ATM/IAM (Python)
  agent-layer-2/             # Meta Analyzer — correlation, verification, risk scoring (Python)
  aegis-soar-engine/         # SOAR decision engine — playbooks, connectors, rollback (Python)
  aegis-staging-sandbox/     # Staging simulation APIs for safe response testing
  dashboard/                 # SOC Dashboard — Go backend + React frontend
  aegis-bank-terraform/      # AWS Terraform modules (hackathon + production profiles)
```

### Step 2 — Quick start with Docker Compose

The [`aegis-bank-deployment`](https://github.com/Little-Boy-s-Aegis/aegis-bank-deployment) repository is the **single entry point** that orchestrates all microservices. It pulls/builds all service images and wires them together.

```bash
cd aegis-bank-deployment

# Copy environment template
cp .env.example .env

# Review and edit .env — set API keys, database passwords, etc.
# At minimum, configure:
#   - OPENAI_API_KEY or BEDROCK credentials (for AI agents)
#   - Database passwords
#   - JWT secrets

# Build and start the full platform
docker compose up --build -d
```

> [!IMPORTANT]
> Review every value in `.env` before use. Default and example credentials are for isolated local development only. Do not expose the stack — or its simulated vulnerable modes — to an untrusted network.

### Step 3 — Access the platform

Once all containers are healthy, access the services:

| Service | URL | Description |
|---|---|---|
| Nginx Gateway | `http://localhost/` | Main entry point, routes to all services |
| Banking Web Portal | `http://localhost/bank` | Customer-facing banking application |
| SOC Dashboard | `http://localhost/soc` | Security Operations Center workspace |
| Banking API | `http://localhost/api` | Spring Boot REST API (Swagger/OpenAPI) |
| Kafka UI | `http://localhost/kafka-ui` | Kafka topic browser and consumer groups |

> [!NOTE]
> Exact ports and paths may vary depending on your `.env` configuration. Check the `docker-compose.yml` and Nginx config in `aegis-bank-deployment` for the definitive service mapping.

### What starts locally

The deployment composes the following services:

| Layer | Services |
|---|---|
| **Frontend** | Customer web portal (Next.js), SOC dashboard (React) |
| **Backend** | Banking API (Spring Boot), SOC backend (Go) |
| **AI Agents** | Layer 1 sensor agents, Layer 2 meta analyzer, SOAR engine |
| **Data** | PostgreSQL, Redis, Qdrant (vector DB) |
| **Event Backbone** | 3-node Kafka KRaft cluster, Fluent Bit, log parser |
| **Security** | OPA (Open Policy Agent), Vault, staging sandbox |
| **Gateway** | Nginx reverse proxy with security headers |

### Useful operating commands

```bash
# Follow all platform logs
docker compose logs -f

# Watch specific layers
docker compose logs -f kafka-1 kafka-2 kafka-3 fluent-bit log-parser    # Event pipeline
docker compose logs -f agent-layer-1 agent-layer-2 soar-engine           # AI & SOAR
docker compose logs -f bank-backend bank-web-client                      # Banking apps
docker compose logs -f soc-backend soc-frontend                          # SOC Dashboard

# Check service health
docker compose ps

# Restart a specific service
docker compose restart agent-layer-1

# Stop services without deleting persisted data
docker compose down

# Full reset — delete all volumes and rebuild
docker compose down -v && docker compose up --build -d
```

### Troubleshooting

| Issue | Solution |
|---|---|
| Containers keep restarting | Check `docker compose logs <service>` for errors. Ensure `.env` is configured correctly. |
| Kafka not ready | Kafka KRaft cluster needs ~30s to elect a leader. Wait and retry. |
| AI agents failing | Verify API keys (OpenAI/Bedrock) are set in `.env`. |
| Out of memory | Increase Docker memory to 8 GB+ in Docker Desktop settings. |
| Port conflicts | Check if ports 80, 5432, 6379, 9092 are already in use. Adjust in `.env`. |

### Kubernetes deployment

For Kubernetes-based deployment, `aegis-bank-deployment` also includes:

- **Kustomize** base + overlays for local clusters
- **Helm** chart with configurable values for all services
- **Kubernetes manifests** for production-like environments

```bash
# Kustomize (local overlay)
kubectl apply -k aegis-bank-deployment/k8s/overlays/local

# Helm
helm install aegis aegis-bank-deployment/helm/aegis-platform -f values-local.yaml
```

### AWS cloud deployment

For AWS deployment, use the [`aegis-bank-terraform`](https://github.com/Little-Boy-s-Aegis/aegis-bank-terraform) repository:

```bash
cd aegis-bank-terraform

# Hackathon profile — single AZ, ~$30-80/month
terraform init
terraform plan -var-file=profiles/hackathon.tfvars
terraform apply -var-file=profiles/hackathon.tfvars

# Production profile — multi-AZ, PrivateLink, full security stack
terraform plan -var-file=profiles/production.tfvars
terraform apply -var-file=profiles/production.tfvars
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
