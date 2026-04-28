# ☁️ DevOps & Cloud Infrastructure Skills Suite
### Derived from [anthropics/claude-code](https://github.com/anthropics/claude-code)

![Domain](https://img.shields.io/badge/Domain-DevOps%20&%20Cloud%20Infrastructure-blue?style=for-the-badge)
![Commands](https://img.shields.io/badge/Commands-10-blue?style=for-the-badge)
![Workflows](https://img.shields.io/badge/Workflows-5-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

> **Adaptation of `anthropics/claude-code` for DevOps & Cloud Infrastructure use cases.**
> Source focus: _official Claude Code CLI, examples, plugins, scripts_

---

## What This Skill Suite Does

CI/CD pipelines, container orchestration, IaC, monitoring and incident response.

This collection provides **10 specialised commands** and
**5 multi-step workflows**, all with a consistent
structured-output UI so you always know exactly where you are and what to do next.

---

## Quick Install

```bash
# Clone this skill
cp -r . ~/.claude/skills/r00-anthropics-claude-code--devops/

# Register in Claude Code
# In a Claude Code session:
/read ~/.claude/skills/r00-anthropics-claude-code--devops/SKILL.md
```

---

## Commands

| Command | Description |
|---------|-------------|
| `/pipeline-generate` | Generate GitHub Actions / GitLab CI / Jenkins pipeline from repo analysis |
| `/docker-optimize` | Multi-stage Dockerfile optimisation for image size and build cache efficiency |
| `/k8s-manifest` | Production-ready Kubernetes manifests with HPA, PDB and NetworkPolicies |
| `/terraform-scaffold` | Terraform module scaffold with variables, outputs and state backend config |
| `/monitor-setup` | Prometheus + Grafana alerting rules from SLO definitions |
| `/incident-runbook` | Auto-generated incident runbook from service topology and past incidents |
| `/cost-optimize` | Cloud cost anomaly detection and right-sizing recommendations |
| `/security-scan` | Container image, IaC and dependency vulnerability scan with CVSS triage |
| `/secrets-audit` | Detect hardcoded secrets, rotate recommendations and vault migration plan |
| `/rollback-plan` | Deployment rollback plan with canary thresholds and feature-flag kill switches |

**Usage:**
```bash
/pipeline-generate <target>
/docker-optimize --scope full --output md
```

---

## Workflows (Multi-step)

| Workflow | Description |
|----------|-------------|
| `release-pipeline` | Full GitOps release: tag → build → scan → stage → promote → monitor |
| `disaster-recovery` | DR drill: failover, RTO/RPO validation and runbook update workflow |
| `infra-migration` | Lift-and-shift to cloud-native: assessment → IaC → cut-over checklist |
| `sre-onboarding` | New service onboarding: SLOs, dashboards, runbooks and on-call rotation |
| `devsecops-pipeline` | Shift-left security: SAST, DAST, SCA and policy-as-code gate workflow |

**Usage:**
```bash
/workflows:release-pipeline <target> --scope full
```

---

## UI Design

All commands display structured output with:

- **Progress panels** — real-time step tracking
- **Findings tables** — sorted by severity (🔴🟠🟡🟢)
- **Action checklists** — quick wins → medium-term → strategic
- **Summary cards** — at-a-glance metrics after each command


## Progress Display Example

```
╔══════════════════════════════════════════════════╗
║  Deployment Pipeline  —  api-service v2.4.1      ║
╠══════════════════════════════════════════════════╣
║  Build          ✓  2m 14s                         ║
║  Unit tests     ✓  1m 08s   (342/342 passed)      ║
║  Security scan  ✓  3m 42s   (0 critical, 2 low)   ║
║  Push image     ✓  0m 47s                         ║
║  Deploy staging ⟳  Running …                      ║
║  Smoke tests    ░  Pending                        ║
║  Promote prod   ░  Pending                        ║
╚══════════════════════════════════════════════════╝

CRITICAL ALERTS
  ✗  CVE-2024-1234  nginx:1.24  CVSS 9.8  → Upgrade to 1.26
  ⚠  CVE-2024-5678  openssl     CVSS 6.5  → Patch available
```


---

## Interaction Pattern

Every command follows this 5-step structure:

```
① Scope Confirmation  — verify target and options with user
② Live Analysis       — progress bar while working
③ Findings Table      — structured results sorted by impact
④ Action Plan         — prioritised, time-boxed recommendations
⑤ Next Steps          — suggested follow-up commands
```

---

## Source Repository

This suite is derived from
**[anthropics/claude-code](https://github.com/anthropics/claude-code)**
which focuses on: _official Claude Code CLI, examples, plugins, scripts_.

Improvements in this adaptation:
- Domain-specific command vocabulary for DevOps & Cloud Infrastructure
- Enhanced structured output with visual progress tracking
- Prioritised action plans with time estimates
- Workflow orchestration for end-to-end processes
- Consistent UI conventions across all commands

---

## License

MIT — free to use, modify and distribute.
