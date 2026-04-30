# 🚀 JobValidator: Agentic Career Orchestrator

**A resilient, multi-agent state machine that deterministically evaluates your resume against job descriptions and autonomously engineers a gap-bridging strategy.**

---

### 🌟 The Value Proposition

Applying for jobs in the modern tech landscape often feels like throwing resumes into an ATS black box. **JobValidator** changes the paradigm by treating career alignment as a deterministic engineering problem. 

Instead of relying on fragile keyword-counting algorithms, this tool utilizes **Agentic AI** to deeply analyze semantic alignment. It provides brutal honesty: a hard percentage score. If you fall short, the state machine autonomously transitions to a "Critic Agent" that acts as your personal career strategist, outlining exact technical gaps and prescribing highly targeted upskilling paths. Stop guessing; start targeting.

### 🧠 Agentic Architecture & State Machine Flow

JobValidator is heavily inspired by **LangGraph** principles, operating as a deterministic state machine rather than a linear script:

1. **The Ingestion State:** Secures API endpoints and dynamically routes requests, ensuring the system is ready to process unstructured text.
2. **The Scoring Agent (Node 1):** A primary LLM evaluates the resume against the JD, outputting a strict, hallucination-free numerical value.
3. **The Conditional Router (The Edge):** The state machine evaluates the score against your predefined threshold. 
    * *If Score >= Threshold:* The workflow halts, returning a "PASS".
    * *If Score < Threshold:* The workflow routes to the Critic Agent.
4. **The Critic Agent (Node 2):** A secondary, highly critical agent analyzes the deficit. It cross-references the required JD skills against the resume's missing components and outputs a deterministic 3-point gap analysis, complete with actionable upskilling tasks.

### ✨ Key Features

* 🕸️ **Multi-Agent Orchestration:** Utilizes isolated AI agents for specific tasks (Scoring vs. Critiquing) to prevent context pollution and hallucination.
* 🛡️ **Dynamic Failover Routing:** Built for absolute high availability. Automatically catches `503/404` server errors and seamlessly reroutes requests across a heterogeneous topology of Gemini models.
* ⚙️ **Deterministic Guardrails:** Forces unstructured, conversational AI models to return strict numerical values and actionable data. 
* 🔒 **Zero-Leak Privacy:** Engineered for Google Colab with absolute data privacy. API keys are managed exclusively through encrypted Colab Secrets, ensuring your credentials never touch the repository.

### 🛠️ Technology Stack
* **Language:** Python
* **AI & Inference:** Google Gemini API (Dynamic Fallback Router)
* **Architecture:** State Machine Orchestration / Agentic Workflows
* **Environment:** Google Colab

### 🚀 Getting Started

1. Clone this repository or open the notebook directly in Google Colab.
2. Add your Google Gemini API key to your Colab Secrets as `geminiKey`.
3. Paste your target Job Description and your raw Resume text into the designated fields.
4. Set your target matching threshold (e.g., `50%`).
5. Run the orchestrator and let the agents perform their analysis.

---
*Built with 💻 and ☕ by [Kiran Kulkarni](https://github.com/kiranUlhasKulkarni) | Exploring the intersection of Agentic AI and System Resiliency.*
