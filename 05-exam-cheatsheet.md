# AB-100 Exam Cheatsheet

> Print-friendly. The 60-second reset before exam time.

## The 3 domains

| Domain | Weight | Key topics |
|---|---|---|
| Plan | 33% | Discovery, architecture choice, identity, environments, cost |
| Design | 34% | Topics, generative answers, knowledge, connectors, multi-agent, RAI |
| Deploy | 33% | Channels, ALM, monitoring, adoption, governance |

## Copilot Studio building blocks

- **Topics** - scripted flows.
- **Generative answers** - LLM grounded on knowledge sources.
- **Knowledge sources** - SharePoint, web, OneDrive, Dataverse, custom, Graph.
- **Actions** - connectors / Power Automate / MCP / Azure OpenAI tools.
- **Variables** - conversation / bot / global scope.
- **Channels** - M365 Copilot Chat, Teams, web, custom (DirectLine), voice.

## Architecture decision rules

- Q&A on docs -> Generative answers + knowledge.
- Scripted dialog -> Topics.
- Action in 3rd-party -> Connector / Power Automate.
- Multi-step autonomous -> Agentic with multiple tools.
- Cross-app one-front-door -> Multi-agent orchestration.

## Identity matrix

| Channel | Auth |
|---|---|
| Internal Teams / M365 Copilot | Microsoft Entra ID |
| Public web | None or OAuth |
| Custom mobile app | DirectLine + bearer / API key |
| 3rd-party SaaS | Manual OAuth / API key |

## Environments and ALM

- Dev -> Test -> UAT -> Prod via solutions.
- **Managed solution** in prod.
- **PAC CLI** + GitHub Actions / Azure DevOps for pipelines.
- **Managed environments** add solution checker, DLP, capacity reporting.
- **Connection references** abstract per-env credentials.

## Pricing model

- Copilot Studio: per-message capacity unit (CU); packs of 25k / 100k.
- Premium connectors: Power Platform per-user / per-flow.
- M365 Copilot license: per user / month (separate).
- Azure OpenAI (custom model): token / PTU.

## Responsible AI

- Microsoft Responsible AI Standard v2.
- Impact Assessments per use case.
- Copilot Studio content moderation slider.
- Microsoft Copyright Commitment for output IP.

## Question-pattern translator

| Wording | Answer |
|---|---|
| "agent answers from internal docs" | Generative answers + SharePoint knowledge |
| "guided FAQ-style chat" | Topics |
| "trigger ServiceNow ticket" | Connector / Power Automate flow |
| "internal employee agent identity" | Microsoft Entra ID |
| "isolate environments" | Power Platform environments |
| "promote agent" | Solution + PAC CLI |
| "tighten LLM safety" | Content moderation slider (high) |
| "fan-out to specialist agents" | Multi-agent orchestration |
| "fine-tune M365 Copilot for org tone" | Microsoft 365 Copilot Tuning |
| "free tool to find oversharing" | M365 Copilot Optimization Assessment |
| "rich UI element in chat" | Adaptive card |
| "block sensitive connector combos" | DLP policies |
| "deep tracing of prompts" | Application Insights |
| "central governance toolkit" | CoE Starter Kit |

## 60-second reset

1. Three domains: Plan / Design / Deploy.
2. Copilot Studio: Topics + Generative answers + Knowledge + Actions.
3. Channels: M365 Copilot Chat, Teams, web, DirectLine, voice.
4. ALM: Solutions, PAC CLI, environments, managed solution in prod.
5. Governance: DLP, managed environments, CoE kit.
6. Multi-agent orchestration for cross-domain front doors.
7. Microsoft 365 Copilot Tuning for org-specific style/facts.
8. Microsoft Copyright Commitment + Responsible AI Impact Assessments.

---

[Master Index](00-MASTER-INDEX.md)
