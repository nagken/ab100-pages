# AB-100 Learn Summaries

> Microsoft Learn summaries grouped by domain.

## Domain 1 - Plan AI-Powered Business Solutions

**Discovery and architecture choice.** Start by mapping the business problem to a persona, the user journey, the knowledge needed, and the actions required. The architectural choice is whether to use Topics (scripted flow), Generative answers + knowledge sources (RAG Q&A), Connectors and Power Automate (actions), agentic orchestration (autonomous multi-step), or multi-agent orchestration (cross-domain front door). Identity options range from no auth (public site) to Microsoft Entra ID (internal employees, identity flows to backend). Sensitive data is governed via Power Platform DLP policies (Business / Non-business / Blocked groups), Microsoft Purview labels, and the M365 Copilot Optimization Assessment for SharePoint oversharing. Power Platform environments isolate dev/test/UAT/prod; managed environments add solution checker, capacity reporting, and DLP enforcement. Pricing: Copilot Studio uses per-message capacity units (CU), and premium connectors require Power Platform licenses; Microsoft 365 Copilot is a separate per-user license.

## Domain 2 - Design AI-Powered Business Solutions

**Building agents in Copilot Studio.** Custom agents combine Topics (authored conversation flows), Generative answers (RAG against knowledge sources), Knowledge sources (SharePoint, public website, OneDrive, Dataverse, custom uploads, Microsoft Graph), Actions (connectors, Power Automate flows, MCP servers / skills, Azure OpenAI tools), Variables (conversation / bot / global), and Channels (Microsoft 365 Copilot Chat, Teams, web demo, DirectLine custom apps, voice). Multi-agent orchestration uses an orchestrator agent to route requests to specialist agents. Adaptive cards provide rich UI in Teams. Memory uses conversation, bot, and global variables. Responsible AI guardrails include the Copilot Studio content moderation slider (low/medium/high), generative answers confidence fallback to a Topic or human, built-in jailbreak / prompt-injection mitigation, and Application Insights telemetry for prompt + response audit. Microsoft 365 Copilot Tuning fine-tunes M365 Copilot on org-specific tone and facts (separate from RAG).

## Domain 3 - Deploy AI-Powered Business Solutions

**Channels, ALM, monitoring, adoption.** Publish channels include Microsoft 365 Copilot Chat (primary internal channel), Microsoft Teams (sideloaded via admin), web demo / iframe, custom DirectLine apps, voice / telephony, and select social messaging. ALM uses Power Platform Solutions to package agents, connectors, flows, and config; Power Platform CLI (PAC CLI) integrates with Git source control; GitHub Actions and Azure DevOps templates automate Dev -> Test -> UAT -> Prod promotion. Managed solutions deploy in production. Connection references abstract per-environment credentials. Monitoring combines built-in Copilot Studio analytics (sessions, resolution rate, escalation rate, top topics) with Application Insights for end-to-end traces, Power Platform admin center for capacity / DLP / audit, and Microsoft Purview for sensitive data flow audit. Adoption uses the CoE Starter Kit for governance, champion networks, maker training, and DLP policy reviews. KPIs include sessions/day, resolution rate, escalation rate, CSAT, cost per session, and top failed topics. Pilot to scale follows 4-8 weeks pilot -> 8-12 weeks Wave 1 -> quarterly Wave 2+ -> continuous Optimize.

---

[Master Index](00-MASTER-INDEX.md)
