# AB-100 Extra Concepts

> Subtle distinctions that show up in exam wording.

## Agent vs Copilot vs Bot

| Term | Capability |
|---|---|
| **Bot** (classic) | Scripted topic flows |
| **Copilot** | Conversational AI helper, often grounded on knowledge |
| **Agent** | Autonomous; takes multi-step actions with tools |

## Generative answers vs Topics

| Use | Generative answers | Topics |
|---|---|---|
| Open-ended Q&A | y | n |
| Strict regulated dialog | n | y |
| Easy maintenance | y | n |
| Predictable output | n | y |

In practice, mix: Topic captures intent, generative answers within branches.

## Knowledge != training

- Knowledge sources = **RAG** (retrieval at runtime).
- Microsoft 365 Copilot Tuning = real fine-tuning of model variant for tone/facts.

## MCP - Model Context Protocol

Open standard for letting agents call external tools through a uniform interface. Copilot Studio supports MCP servers as **skills** / actions.

## Power Platform connector tiers

| Tier | License need |
|---|---|
| Standard | Included in baseline |
| Premium | Power Apps / Power Automate premium license |
| Custom | Build your own |
| Independent Publisher | Community-built |

## DLP policy mechanics

- Connectors classified into **Business** / **Non-business** / **Blocked**.
- Within the same flow / agent, connectors from different groups cannot be combined.
- Helps prevent data leak (e.g., SharePoint + Twitter in same flow).

## ALM artifacts

| Artifact | Role |
|---|---|
| **Solution** | Package of components to promote |
| **Unmanaged solution** | Editable, dev only |
| **Managed solution** | Locked components; deploy in prod |
| **Connection reference** | Abstract connection (per env credential) |
| **Environment variable** | Per-env config value |

## Responsible AI moderation slider

- **Low** - most permissive; more creative.
- **Medium** - balanced (default).
- **High** - strictest; may refuse more often.

## Fallback orchestration

- When generative answers confidence is low -> fallback to a Topic or human handoff.
- Handoff via Microsoft Teams transfer, Dynamics 365 Customer Service queue.

## Microsoft Graph connector

- Lets Microsoft Search / M365 Copilot index 3rd-party data (e.g. ServiceNow, Confluence).
- Different from Power Platform connectors (which take actions, not index data).

## Voice + telephony

- Power Virtual Agents voice channel (preview / GA path) lets agents serve phone calls.
- Configure SSML for prosody control.

---

[Master Index](00-MASTER-INDEX.md)
