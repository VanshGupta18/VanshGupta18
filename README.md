<div align="center">

<img src="https://github.com/VanshGupta18.png" width="120" style="border-radius:50%"/>

# Vansh Gupta

**AI Engineer · Production-Grade Intelligent Systems**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vanshgupta1810/)
[![Email](https://img.shields.io/badge/Email-vanshgupta1810%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:vanshgupta1810@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-VanshGupta18-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/VanshGupta18)

*Building intelligent systems that move from notebook to production — RAG pipelines, LLM agents, financial analytics, and NLP applications.*

<br/>

<img src="https://github-readme-stats.vercel.app/api?username=VanshGupta18&show_icons=true&theme=tokyonight&hide_border=true" height="165"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=VanshGupta18&layout=compact&theme=tokyonight&hide_border=true" height="165"/>

</div>

---

## About Me

I'm an AI Engineer focused on building reliable, production-grade systems that turn large language models into practical tools. My work spans the full lifecycle — from designing retrieval pipelines and agentic workflows to deploying full-stack APIs and building domain-specific NLP applications.

Right now I'm deep in **earnings call intelligence** and **corporate compliance automation**, two domains where AI can meaningfully reduce analyst workload and governance risk. I'm also actively exploring geopolitical risk modeling and domain-specific fine-tuning.

---

## 🏆 Hackathon Recognition

| Award | Event | Organizer | Year |
|---|---|---|---|
| 🥈 **Finalist** | Meta PyTorch OpenEnv Hackathon | Meta · PyTorch | 2026 |
| 🥇 **Innovation Award** | Agentic AI Hackathon | Ulster University, UK | 2025 |

---

## Tech Stack

| Layer | Tools |
|---|---|
| **Languages** | Python · TypeScript · Node.js |
| **AI / LLM** | LangChain · Groq · Hugging Face · Prompt Engineering · PyTorch Geometric |
| **Backend** | FastAPI · Fastify · REST APIs · SSE |
| **Data & ML** | Pandas · Scikit-learn · PyTorch · Optuna · NeuroKit2 |
| **Infrastructure** | Docker · PostgreSQL · pgvector · AWS S3 · Supabase |
| **Domains** | RAG · Agentic AI · NLP · Financial Analytics · Medical ML · RL Environments |

---

## Featured Projects

### 💬 [GINA — Grounded Insight from Natural Language Analytics](https://github.com/VanshGupta18/Gina_cfp)
> **Conversational analytics platform that turns plain-English questions into grounded, SQL-backed answers over your own data**

GINA lets users upload a CSV, ask questions in natural language, and receive answers backed by real SQL execution — not model hallucination. It follows **Table-Augmented Generation (TAG)**: the model reasons *with* the table, not instead of it. A live streaming pipeline (planner → SQL → execution → narration) runs transparently over SSE, so users can see exactly how their answer was produced.

**Key highlights:**
- PII shield runs client-side before any data leaves the browser
- Tiered SQL generation: deterministic templates → Groq → Hugging Face, with automatic fallback
- pgvector-backed semantic schema profiling for accurate query routing
- Full SQL disclosure and expandable verification queries in the UI
- Deployed and live with Supabase Auth, AWS S3, and PostgreSQL

`Next.js` `Fastify` `PostgreSQL` `pgvector` `Groq` `Hugging Face` `AWS S3` `SSE` `TypeScript`

---

### 🤖 [Corporate Compliance Environment](https://github.com/VanshGupta18/corporate-compliance-env)
> **Finalist — Meta PyTorch OpenEnv Hackathon 2026 · The first open-source RL training environment for enterprise expense compliance**

An OpenEnv-compliant Reinforcement Learning environment that simulates how a corporate compliance officer audits employee expense claims. The agent receives a ticket, searches a 15-rule policy document, requests missing documents if needed, and resolves each claim with `Approve`, `Reject`, or `Escalate`. Three difficulty tiers — easy, medium, and hard — test progressively more complex multi-turn reasoning.

**Key highlights:**
- Fully OpenEnv-compliant: `reset`, `step`, `state`, `grader`, and `baseline` endpoints all validated
- LLM agent (Llama-3.1-8B) achieves 0.90 / 0.80 / 0.70 on easy / medium / hard vs. rule-based baseline of 0.78 / 0.61 / 0.34
- Policy document is a plain `policy.md` — any company can swap in their own rulebook
- Grounded in Indian corporate compliance norms: ₹-denominated limits, GST, WFH, and seniority rules
- Live on Hugging Face Spaces; Dockerized for local deployment

`Python` `FastAPI` `Reinforcement Learning` `LLM Agents` `Docker` `OpenEnv` `Hugging Face`

---

### 📈 [Earning Calls Intelligence](https://github.com/VanshGupta18/earning-calls)
> **Multimodal pipeline that models earnings calls as pressure-driven information environments to extract short-horizon market signals**

Most earnings call analysis flattens the entire transcript into one sentiment score. This project goes further by treating the call as a **pressure-sensitive interaction system** — modeling the moments where a manager's wording, vocal delivery, and response behavior diverge under analyst questioning. Features like `tone_divergence`, `specificity_under_pressure`, and `response_latency` are designed to capture signals that markets may underreact to.

**Key highlights:**
- Speaker diarization with pyannote.audio; transcript alignment with WhisperX
- Structural segmentation into prepared remarks, analyst questions, and management answers — Q&A weighted 3× over scripted remarks during aggregation
- Text (FinBERT), audio (wav2vec2, openSMILE), and interaction features (text–audio divergence, hesitation under pressure)
- Leakage-aware evaluation with strict time-based train/test splits
- Targets: next-day return, 5-day return, realized volatility, earnings surprise, downside risk proxy

`Python` `PyTorch` `LightGBM` `FinBERT` `wav2vec2` `WhisperX` `pyannote.audio` `DuckDB` `Parquet`

---

### 🫀 [ECG Multi-Label Classification](https://github.com/VanshGupta18/ECG-Multi-Label-Classification)
> **Graph Neural Network framework for detecting multiple concurrent cardiac conditions from 12-lead ECG signals**

A medical ML project that reframes ECG analysis as a graph problem. Rather than treating each lead independently, it constructs graph representations of 12-lead signals that capture spatial-temporal correlations — then applies GNN message passing to predict multiple simultaneous cardiac pathologies on the PTB-XL dataset.

**Key highlights:**
- ECG signals converted to graph structures preserving inter-lead spatial relationships
- NeuroKit2 for physiological feature extraction (R-peaks, HRV, waveform morphology)
- Automated hyperparameter tuning with Optuna across GNN architecture configurations
- Multi-label output handles overlapping arrhythmia patterns common in real clinical data
- Evaluated on F1 and AUC-ROC per label — metrics that matter clinically, not just statistically

`Python` `PyTorch Geometric` `NeuroKit2` `Optuna` `Scikit-learn` `PTB-XL` `Medical ML`

---

## Areas of Focus

**🔬 Currently building**
- Pressure-aware multimodal earnings call intelligence (text + audio + interaction)
- OpenEnv-compliant agentic compliance systems with RL and LLM training pipelines (SFT + GRPO)

**🌱 Actively exploring**
- Geopolitical risk modeling using LLMs and structured data
- Domain-specific LLM fine-tuning for finance and legal
- Agentic AI patterns: planning, memory, multi-turn tool use

---

## Get In Touch

I'm open to collaborations on AI engineering projects, especially in financial analytics, agentic systems, or applied NLP.

- 📧 **Email:** [vanshgupta1810@gmail.com](mailto:vanshgupta1810@gmail.com)
- 💼 **LinkedIn:** [vanshgupta1810](https://www.linkedin.com/in/vanshgupta1810/)
- 🐙 **GitHub:** [VanshGupta18](https://github.com/VanshGupta18)

---

<div align="center">
<sub>Building systems that think — one pipeline at a time.</sub>
</div>
