# OAC: Organizational Artificial Consciousness

![Project Status](https://img.shields.io/badge/status-conceptual-blue) ![Version](https://img.shields.io/badge/version-1.0.0-lightgrey) ![License](https://img.shields.io/badge/license-CC--BY--4.0-orange)

**[Available in Arabic](./README-AR.md) | متوفر باللغة العربية**

---

OAC is a theoretical framework and a future-looking blueprint for designing next-generation AI systems. It moves beyond monolithic models by proposing a hierarchical, multi-agent architecture where small, specialized AI "agents" are coordinated by a central "manager" to solve complex problems.

The core philosophy of OAC is the complete **separation of the reasoning engine from the knowledge base**. Instead of building massive models that "know" everything, we aim to build smaller, more efficient "reasoning" models that are masters of thinking, planning, and learning, and that access a vast, external, and updatable knowledge library.

This repository is the central hub for the OAC framework.

```mermaid
graph LR
    subgraph "User Interaction"
        U["fa:fa-user User"]
    end

    subgraph "OAC Core: Reasoning & Delegation"
        M["**fa:fa-sitemap The Manager**<br/>(Strategic Reasoner)"]
    end

    subgraph "Execution: Specialist Agents & Tools"
        subgraph "Specialist Agents"
            direction TB
            A1["fa:fa-code Code Agent"]
            A2["fa:fa-atom Physics Agent"]
            A3["fa:fa-database Memory Agent"]
            A4["..."]
        end
        subgraph "Execution Tools"
            direction TB
            T1["fa:fa-cogs Code Interpreter"]
            T2["fa:fa-globe Web Search"]
            T3["fa:fa-calculator Calculator"]
            T4["fa:fa-server DB Interface"]
        end
    end

    subgraph "Learning & Improvement Loop"
        META["**fa:fa-chart-line Metacognition Agent**<br/>(System Optimizer)"]
    end

    U -- "Request / Response" --> M
    M -- "Task Delegation (A2A)" --> A1
    M -- "Task Delegation (A2A)" --> A2
    M -- "Task Delegation (A2A)" --> A3

    A1 --> T1
    A1 --> T2
    A2 --> T3
    A3 --> T4

    M -- "Logs & Metrics" --> META
    A1 & A2 & A3 -- "Logs & Metrics" --> META
    META -.->|"Improvement<br/>Recommendations"| M

    classDef manager fill:#87CEEB,stroke:#333,stroke-width:2px;
    classDef agent fill:#90EE90,stroke:#333,stroke-width:2px;
    classDef tool fill:#F0E68C,stroke:#333,stroke-width:1px;
    classDef meta fill:#FFA07A,stroke:#333,stroke-width:2px;
    classDef user fill:#D8BFD8,stroke:#333,stroke-width:2px;

    class U user;
    class M manager;
    class A1,A2,A3,A4 agent;
    class T1,T2,T3,T4 tool;
    class META meta;
```

---

## 📚 Project Documents

This repository hosts two primary documents: a detailed manuscript for a deep dive, and a concise research paper for an academic overview.

### 1. The Full Manuscript
*A comprehensive, book-length document detailing the complete architecture, philosophy, and future of the OAC framework.*

- 📖 **Read the Manuscript (English)**: [`MANUSCRIPT-EN.md`](./MANUSCRIPT-EN.md)
- 📖 **قراءة المخطوطة (العربية)**: [`MANUSCRIPT-AR.md`](./MANUSCRIPT-AR.md)


### 2. The Research Paper
*A formal, condensed academic paper summarizing the OAC framework, its implications, and future work.*

- 📄 **Read the Paper (English)**: [`PAPER-EN.md`](./PAPER-EN.md)
- 📄 **قراءة الورقة البحثية (العربية)**: [`PAPER-AR.md`](./PAPER-AR.md) 

---

## Core Principles

- **Hierarchical Structure:** A "manager" agent delegates tasks to specialized "executor" agents.
- **Decoupled Memory:** An external, multi-layered memory ecosystem serves as the single source of truth.
- **Standardized Communication:** Agents communicate via a formal protocol like [A2A (Agent-to-Agent Protocol)](https://a2a-protocol.org/latest/).
- **Continuous Evolution:** The system learns and improves over time through reinforcement learning and self-reflection.