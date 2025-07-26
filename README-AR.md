# OAC: الوعي الاصطناعي التنظيمي (OAC)

![حالة المشروع](https://img.shields.io/badge/status-conceptual-blue) ![الإصدار](https://img.shields.io/badge/version-1.0.0-lightgrey) ![الرخصة](https://img.shields.io/badge/license-CC--BY--4.0-orange)

**[English Version](./README.md)**

---

OAC هو إطار عمل نظري ومخطط مستقبلي لتصميم أنظمة الذكاء الاصطناعي من الجيل القادم. إنه يتجاوز النماذج المتجانسة عبر اقتراح بنية هرمية متعددة الوكلاء، حيث يتم تنسيق "وكلاء" ذكاء اصطناعي متخصصين وصغار الحجم بواسطة "مدير" مركزي لحل المشاكل المعقدة.

تقوم الفلسفة الجوهرية لـ OAC على **الفصل التام بين محرك الاستدلال وقاعدة المعرفة**. فبدلاً من بناء نماذج ضخمة "تعرف" كل شيء، نهدف إلى بناء نماذج "استدلال" أصغر وأكثر كفاءة، تتقن مهارات التفكير، والتخطيط، والتعلم، وتصل إلى مكتبة معرفة خارجية ضخمة وقابلة للتحديث.

هذا المستودع هو المحور المركزي لإطار OAC.

```mermaid
graph LR
    subgraph "User Interaction"
        U["fa:fa-user المستخدم"]
    end

    subgraph "OAC Core: Reasoning & Delegation"
        M["**fa:fa-sitemap المدير**<br/>(المُستدل الاستراتيجي)"]
    end

    subgraph "Execution: Specialist Agents & Tools"
        subgraph "الوكلاء المتخصصون"
            direction TB
            A1["fa:fa-code وكيل البرمجة"]
            A2["fa:fa-atom وكيل الفيزياء"]
            A3["fa:fa-database وكيل الذاكرة"]
            A4["..."]
        end
        subgraph "أدوات التنفيذ"
            direction TB
            T1["fa:fa-cogs مفسر الأكواد"]
            T2["fa:fa-globe البحث على الإنترنت"]
            T3["fa:fa-calculator حاسبة"]
            T4["fa:fa-server واجهة قواعد البيانات"]
        end
    end

    subgraph "Learning & Improvement Loop"
        META["**fa:fa-chart-line وكيل ما وراء المعرفة**<br/>(محسّن النظام)"]
    end

    U -- "طلب / رد" --> M
    M -- "تفويض المهام (A2A)" --> A1
    M -- "تفويض المهام (A2A)" --> A2
    M -- "تفويض المهام (A2A)" --> A3

    A1 --> T1
    A1 --> T2
    A2 --> T3
    A3 --> T4

    M -- "سجلات ومقاييس" --> META
    A1 & A2 & A3 -- "سجلات ومقاييس" --> META
    META -.->|"توصيات<br/>التحسين"| M

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

## 📚 مستندات المشروع

يحتوي هذا المستودع على وثيقتين أساسيتين: مخطوطة مفصلة للتعمق في الفكرة، وورقة بحثية موجزة للملخص الأكاديمي.

### 1. المخطوطة الكاملة
*وثيقة شاملة ومفصلة تشرح البنية الكاملة، والفلسفة، ومستقبل إطار OAC.*

- 📖 **قراءة المخطوطة (العربية)**: [`MANUSCRIPT-AR.md`](./MANUSCRIPT-AR.md)
- 📖 **Read the Manuscript (English)**: [`MANUSCRIPT-EN.md`](./MANUSCRIPT-EN.md)


### 2. الورقة البحثية
*ورقة بحثية أكاديمية رسمية وموجزة تلخص إطار OAC، وآثاره، والعمل المستقبلي.*

- 📄 **قراءة الورقة البحثية (العربية)**: [`PAPER-AR.md`](./PAPER-AR.md)
- 📄 **Read the Paper (English)**: [`PAPER-EN.md`](./PAPER-EN.md)

---

### المبادئ الأساسية

- **الهيكل الهرمي:** "مدير" استراتيجي يفوض المهام إلى "وكلاء" خبراء متخصصين.
- **الذاكرة المنفصلة:** نظام بيئي للذاكرة، خارجي ومتعدد الطبقات، يعمل كمصدر وحيد للحقيقة.
- **الاتصال المعياري:** يتواصل الوكلاء عبر بروتوكول رسمي مثل [A2A (Agent-to-Agent Protocol)](https://a2a-protocol.org/latest/).
- **التطور المستمر:** يتعلم النظام ويتحسن بمرور الوقت من خلال التعلم المعزز والتفكير الانعكاسي.