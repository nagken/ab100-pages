# AB-100 Pitfalls and Gotchas

## 1. Knowledge sources != fine-tuning

Knowledge = RAG at runtime. Fine-tuning = Microsoft 365 Copilot Tuning (separate, requires curated docs).

## 2. Generative answers ON without knowledge source = generic LLM

If you turn on generative answers but don't add a knowledge source, the agent answers from base LLM only - no grounding.

## 3. Topics + Generative answers can both fire

Order is determined by orchestration. Authored topics with strong trigger match win; otherwise generative answers fall through.

## 4. DLP policies block at runtime, not build-time

You can save a flow that violates DLP; it fails when invoked. Always test in target environment.

## 5. Default Power Platform environment is shared

Don't develop in default. Create a dedicated dev environment per maker / project.

## 6. Premium connectors require premium license

Standard tier license alone won't run premium connectors. Plan licensing per agent.

## 7. Unmanaged solutions in prod are bad

Always import as **managed solution** in prod. Allows clean uninstall, prevents drift.

## 8. Connection references vs hardcoded connections

If you hardcode connections in Dev solution, prod imports break. Use connection references.

## 9. Microsoft Graph connector != Power Platform connector

Graph connector indexes content into Microsoft Search/M365 Copilot. Power Platform connectors take actions.

## 10. Adoption metrics alone are vanity

Sessions/day means nothing without resolution rate + CSAT.

## 11. CoE Starter Kit isn't an out-of-box managed env

It's a community Power Platform solution - install and configure separately.

## 12. Multi-agent != replacing single agent for everything

Use multi-agent only when you have >=3 distinct domains and a need for one front door.

## 13. Voice channel limitations

Voice has more constraints (latency, no adaptive cards). Plan accordingly.

## 14. Microsoft Copyright Commitment requires guardrails

You must use built-in safety filters and follow guidance. Otherwise indemnification doesn't apply.

## 15. Agent identity != user identity

By default agents run with their own service identity. To filter per-user, configure auth + Microsoft Graph / connector with delegated permissions.

## 16. Application Insights costs money

Plan a sample rate; full ingestion of every prompt + response can be expensive.

---

[Master Index](00-MASTER-INDEX.md)
