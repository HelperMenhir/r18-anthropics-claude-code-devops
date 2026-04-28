        ---
        name: "r00-anthropics-claude-code--devops"
        description: >
          ☁️ DevOps & Cloud Infrastructure skill suite derived from anthropics/claude-code.
          CI/CD pipelines, container orchestration, IaC, monitoring and incident response.
          Provides 10 specialised commands for devops, cloud, docker workflows.
        version: "1.0.0"
        domain: devops
        tags: ["devops", "cloud", "docker", "kubernetes", "ci-cd", "terraform"]
        source: "https://github.com/anthropics/claude-code"
        license: MIT
        ---

        # ☁️ DevOps & Cloud Infrastructure Skill Suite

        > Derived from **anthropics/claude-code** · Focus: _official Claude Code CLI, examples, plugins, scripts_

        ## Overview

        This skill provides 10 production-ready commands tailored for
        **DevOps & Cloud Infrastructure** workflows. All commands follow a consistent
        interaction pattern with structured output, progress tracking and
        actionable recommendations.

        ## Available Commands

        - `/pipeline-generate` — Generate GitHub Actions / GitLab CI / Jenkins pipeline from repo analysis
- `/docker-optimize` — Multi-stage Dockerfile optimisation for image size and build cache efficiency
- `/k8s-manifest` — Production-ready Kubernetes manifests with HPA, PDB and NetworkPolicies
- `/terraform-scaffold` — Terraform module scaffold with variables, outputs and state backend config
- `/monitor-setup` — Prometheus + Grafana alerting rules from SLO definitions
- `/incident-runbook` — Auto-generated incident runbook from service topology and past incidents
- `/cost-optimize` — Cloud cost anomaly detection and right-sizing recommendations
- `/security-scan` — Container image, IaC and dependency vulnerability scan with CVSS triage
- `/secrets-audit` — Detect hardcoded secrets, rotate recommendations and vault migration plan
- `/rollback-plan` — Deployment rollback plan with canary thresholds and feature-flag kill switches

        ## Interaction Pattern

        Every command follows this structured response format:

        ```
        1. CONTEXT CHECK   — Verify inputs and confirm scope with user
        2. ANALYSIS        — Deep analysis with live progress display
        3. FINDINGS TABLE  — Structured results with severity / priority
        4. RECOMMENDATIONS — Prioritised action list (quick wins first)
        5. NEXT STEPS      — Suggested follow-up commands
        ```

        ## UI Conventions

        | Symbol | Meaning              |
        |--------|----------------------|
        | ✓      | Passed / complete    |
        | ✗      | Failed / critical    |
        | ⚠      | Warning / review     |
        | ⟳      | In progress          |
        | ░      | Pending              |
        | 🔴     | Critical severity    |
        | 🟠     | High severity        |
        | 🟡     | Medium severity      |
        | 🟢     | Low / informational  |

        Progress bars use block characters:
        `[████████░░] 80%`

        ## Quick Start

        ```bash
        # Install this skill
        cp -r . ~/.claude/skills/r00-anthropics-claude-code--devops/

        # In Claude Code
        /read ~/.claude/skills/r00-anthropics-claude-code--devops/SKILL.md
        ```

        Then simply describe your task and Claude will route to the
        appropriate command automatically.
