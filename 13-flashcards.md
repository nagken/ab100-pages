# AB-100 Flashcards

> Click each card to flip.

<section class="fc-section" data-fc-title="Plan">

<div class="flashcard"><div class="fc-q">What's the difference between an agent, Copilot, and a bot?<div class="fc-a">Bot = scripted topics; Copilot = conversational helper grounded on knowledge; <strong>agent = autonomous AI with tools and multi-step actions</strong>.</div></div></div>

<div class="flashcard"><div class="fc-q">Which auth model for an internal employee agent?<div class="fc-a"><strong>Microsoft Entra ID</strong> - flow user identity to backend so per-user security holds.</div></div></div>

<div class="flashcard"><div class="fc-q">How do you isolate dev / test / prod for agents?<div class="fc-a"><strong>Power Platform environments.</strong> Promote via Solutions.</div></div></div>

<div class="flashcard"><div class="fc-q">Free tool to find SharePoint oversharing risks before deploying Copilot?<div class="fc-a"><strong>Microsoft 365 Copilot Optimization Assessment.</strong></div></div></div>

<div class="flashcard"><div class="fc-q">Block sensitive connector combinations?<div class="fc-a"><strong>DLP policies</strong> (Business / Non-business / Blocked groups).</div></div></div>

</section>

<section class="fc-section" data-fc-title="Design">

<div class="flashcard"><div class="fc-q">Open-ended Q&A on internal docs - which Copilot Studio capability?<div class="fc-a"><strong>Generative answers + knowledge sources</strong> (RAG).</div></div></div>

<div class="flashcard"><div class="fc-q">Tightly scripted dialog?<div class="fc-a"><strong>Topics</strong> (trigger phrases + branches).</div></div></div>

<div class="flashcard"><div class="fc-q">Trigger an action in ServiceNow?<div class="fc-a"><strong>Connector or Power Automate flow.</strong></div></div></div>

<div class="flashcard"><div class="fc-q">Tighten LLM safety in Copilot Studio?<div class="fc-a">Set <strong>content moderation slider</strong> to High.</div></div></div>

<div class="flashcard"><div class="fc-q">Variable persisting across conversations for one user?<div class="fc-a"><strong>Bot variable.</strong></div></div></div>

<div class="flashcard"><div class="fc-q">One front door routing to specialist agents?<div class="fc-a"><strong>Multi-agent orchestration</strong> with an orchestrator agent.</div></div></div>

<div class="flashcard"><div class="fc-q">Fine-tune Microsoft 365 Copilot for org-specific tone and facts?<div class="fc-a"><strong>Microsoft 365 Copilot Tuning</strong> (different from RAG knowledge).</div></div></div>

<div class="flashcard"><div class="fc-q">Rich UI element in chat (buttons, image, choices)?<div class="fc-a"><strong>Adaptive card.</strong></div></div></div>

</section>

<section class="fc-section" data-fc-title="Deploy">

<div class="flashcard"><div class="fc-q">Package an agent for promotion across environments?<div class="fc-a"><strong>Solution</strong> (managed solution recommended for prod).</div></div></div>

<div class="flashcard"><div class="fc-q">CLI for Power Platform ALM?<div class="fc-a"><strong>PAC CLI</strong> (Power Platform CLI).</div></div></div>

<div class="flashcard"><div class="fc-q">Per-env credentials for the same connector?<div class="fc-a"><strong>Connection references.</strong></div></div></div>

<div class="flashcard"><div class="fc-q">Centralized governance kit for Power Platform?<div class="fc-a"><strong>CoE Starter Kit</strong> (Center of Excellence).</div></div></div>

<div class="flashcard"><div class="fc-q">Where to view conversation analytics?<div class="fc-a">Built-in <strong>Copilot Studio analytics dashboard</strong>; deeper traces in <strong>Application Insights</strong>.</div></div></div>

<div class="flashcard"><div class="fc-q">Adoption KPI vs vanity?<div class="fc-a">Vanity = sessions only. Real KPIs: <strong>resolution rate, escalation rate, CSAT, cost per session</strong>.</div></div></div>

<div class="flashcard"><div class="fc-q">Copilot Studio pricing unit?<div class="fc-a"><strong>Per-message capacity unit</strong> (CU) - packs of 25k or 100k messages/month.</div></div></div>

</section>

---

[Master Index](00-MASTER-INDEX.md)
