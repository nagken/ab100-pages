# AB-100 Architectures

## 1. Custom Copilot agent (single agent)

```mermaid
flowchart LR
    User[User in Teams / M365 Copilot]
    User --> Agent[Custom Copilot Studio agent]
    Agent --> Topics[Topics]
    Agent --> Gen[Generative answers]
    Gen --> KB[Knowledge:<br/>SharePoint, Web, OneDrive,<br/>Dataverse, Graph]
    Agent --> Actions[Actions:<br/>connectors, Power Automate,<br/>MCP, Azure OpenAI tools]
    Actions --> Backend[Backend systems:<br/>ServiceNow, SAP, Salesforce, etc.]
```

## 2. Multi-agent orchestration

```mermaid
flowchart LR
    User[User]
    User --> Orch[Orchestrator agent]
    Orch -- "intent: HR" --> HR[HR specialist]
    Orch -- "intent: IT" --> IT[IT specialist]
    Orch -- "intent: Finance" --> Fin[Finance specialist]
    HR --> KB1[HR knowledge]
    IT --> KB2[IT knowledge]
    Fin --> KB3[Finance knowledge]
```

## 3. Agent in Microsoft 365 Copilot ecosystem

```mermaid
flowchart TB
    User[Employee]
    User --> M365CP[Microsoft 365 Copilot]
    M365CP --> Custom[Custom Copilot agent]
    Custom --> Knowledge[Knowledge:<br/>SharePoint + Graph]
    Custom --> Action[Power Automate flow]
    Action --> Backend[Backend:<br/>Dynamics, ServiceNow, custom API]
    M365CP --> Graph[Microsoft Graph]
    Graph --> M365Apps[Mail, files, chats]
```

## 4. ALM pipeline

```mermaid
flowchart LR
    Dev[Dev environment] -- Export solution --> Git[Git via PAC CLI]
    Git -- GitHub Actions / Azure DevOps --> Test[Test env]
    Test --> UAT[UAT env]
    UAT --> Prod["Prod env<br/>(managed solution + DLP)"]
    Conn[Connection references] -.-> Test
    Conn -.-> UAT
    Conn -.-> Prod
```

## 5. DLP policy enforcement

```mermaid
flowchart TB
    Policy[DLP policy]
    Policy --> Bus[Business group:<br/>SharePoint, Dataverse, Graph]
    Policy --> Non[Non-business group:<br/>Twitter, Facebook]
    Policy --> Blk[Blocked group:<br/>Banned connectors]
    Flow[Power Automate flow]
    Flow -- "uses connectors only<br/>within one group" --> Allowed[Allowed]
    Flow -- "mixes Business + Non-business" --> Denied[Denied at runtime]
```

## 6. Telemetry pipeline

```mermaid
flowchart LR
    Agent[Copilot Studio agent]
    Agent --> Conv["Conversation analytics<br/>(built-in)"]
    Agent --> AI[Application Insights]
    AI --> KQL[KQL queries]
    AI --> Workbook[Workbook dashboard]
    Agent --> PowerBI[Power BI]
    Agent --> Purview[Microsoft Purview audit]
```

## 7. Managed environment governance

```mermaid
flowchart TB
    ME[Managed environment]
    ME --> Checker[Solution checker]
    ME --> DLP[DLP enforcement]
    ME --> Capacity[Capacity reporting]
    ME --> Sharing[Sharing limits]
    ME --> Audit[Audit log]
```

---

[Master Index](00-MASTER-INDEX.md)
