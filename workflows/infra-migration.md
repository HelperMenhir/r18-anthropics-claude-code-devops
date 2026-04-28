---
model: claude-sonnet-4-6
type: workflow
domain: devops
source_repo: anthropics/claude-code
---

# ☁️ Workflow: Infra Migration

> **Lift-and-shift to cloud-native: assessment → IaC → cut-over checklist**

## Overview

This multi-step workflow orchestrates the full **infra migration**
process for DevOps & Cloud Infrastructure. Each step has clear inputs, outputs and
success criteria displayed via structured UI panels.

## Workflow Steps

| # | Phase | Description | Command |
|---|-------|-------------|---------|
| 1 | **Discovery** | Gather context, define scope and success criteria | `/infra-migration-step-1` |
| 2 | **Audit** | Run all relevant analysis commands in parallel | `/infra-migration-step-2` |
| 3 | **Prioritisation** | Score findings by impact × effort matrix | `/infra-migration-step-3` |
| 4 | **Planning** | Build phased action plan with owners and timelines | `/infra-migration-step-4` |
| 5 | **Execution** | Step-by-step guided execution with checkpoints | `/infra-migration-step-5` |
| 6 | **Validation** | Verify outcomes against success criteria | `/infra-migration-step-6` |
| 7 | **Reporting** | Generate stakeholder report with before/after metrics | `/infra-migration-step-7` |

## Starting the Workflow

```bash
/workflows:infra-migration [target] [options]
```

**Options:**
- `--scope [full|quick|targeted]` — analysis depth (default: full)
- `--output [md|json|html]` — report format (default: md)
- `--notify [slack|email|none]` — completion notification

## Workflow Dashboard

```
╔══════════════════════════════════════════════════════════╗
║  WORKFLOW: INFRA-MIGRATION                              ║
╠══════════════════════════════════════════════════════════╣
║  Step 1/7  Discovery        ✓  Completed  2m 14s        ║
║  Step 2/7  Audit            ✓  Completed  8m 47s        ║
║  Step 3/7  Prioritisation   ⟳  Running …               ║
║  Step 4/7  Planning         ░  Pending                  ║
║  Step 5/7  Execution        ░  Pending                  ║
║  Step 6/7  Validation       ░  Pending                  ║
║  Step 7/7  Reporting        ░  Pending                  ║
╠══════════════════════════════════════════════════════════╣
║  Overall:  [████████░░]  43%   ETA: ~22 min             ║
╚══════════════════════════════════════════════════════════╝
```

## Completion Report Template

At the end of the workflow Claude generates:

```markdown
## Infra Migration — Completion Report

**Date:** {date}
**Duration:** {duration}
**Scope:** {scope}

### Executive Summary
{2-3 sentence summary for stakeholders}

### Key Findings
| Priority | Finding | Impact | Owner | Due |
|----------|---------|--------|-------|-----|

### Before / After Metrics
| Metric | Before | After | Delta |
|--------|--------|-------|-------|

### Next Review
Recommended follow-up: {date + 30 days}
```
