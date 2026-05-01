# 🔬 ResearchMind — Multi-Agent AI Research System

## 🚀 Overview

ResearchMind is a **multi-agent AI system** that autonomously performs end-to-end research on any topic by orchestrating specialized agents for:

* Web search
* Content extraction
* Report generation
* Critical evaluation

Unlike traditional single-model workflows, this system implements a **collaborative agent pipeline**, where multiple AI agents interact to produce **structured, high-quality research outputs**.

---

## 🎯 Problem Statement

Modern research workflows are:

* Time-consuming
* Fragmented across multiple tools
* Dependent on manual synthesis

This project automates the entire pipeline:

> Discover → Read → Synthesize → Evaluate

---

## 🧠 Key Idea

Instead of using one LLM, the system decomposes the task into **specialized agents**, each responsible for a distinct capability.

```text id="p2m8jf"
User Query
   ↓
Search Agent → Reader Agent → Writer Chain → Critic Chain
   ↓
Final Research Report + Evaluation
```

---

## 🏗️ System Architecture

### 1. Search Agent

* Uses Tavily API for real-time web search
* Retrieves:

  * Titles
  * URLs
  * Snippets

### 2. Reader Agent

* Scrapes selected URLs using BeautifulSoup
* Cleans HTML (removes scripts, styles, etc.)
* Extracts meaningful textual content

### 3. Writer Chain

* Uses structured prompting to generate:

  * Introduction
  * Key Findings
  * Conclusion
  * Sources

### 4. Critic Chain

* Evaluates generated report
* Provides:

  * Score (/10)
  * Strengths
  * Weaknesses
  * Final verdict

---

## ⚙️ Tech Stack

* **Python**
* **LangChain** → Agent orchestration
* **OpenAI GPT-4o mini** → Core reasoning engine
* **Streamlit** → Frontend UI
* **Tavily API** → Web search
* **BeautifulSoup** → Web scraping
* **Requests** → HTTP handling
* **Dotenv** → Environment management

---

## 🤖 Agents & Tools

### 🔍 Web Search Tool

* Queries Tavily API
* Returns structured search results

### 📄 Scraper Tool

* Fetches webpage content
* Removes irrelevant HTML
* Returns clean text

---

## 🔄 Execution Pipeline

### Step 1: Search

* Agent gathers relevant web sources

### Step 2: Read

* Extracts deeper content from selected sources

### Step 3: Write

* Generates structured research report

### Step 4: Critique

* Evaluates report quality

---

## 🌐 User Interface

The system includes a **custom-designed Streamlit UI**:

* Minimalist modern design
* Real-time pipeline visualization
* Step-by-step execution tracking
* Expandable raw outputs
* Downloadable reports

👉 Each stage of the pipeline is visible, making the system **interpretable and transparent**

---

## 📈 Key Features

* Multi-agent orchestration
* Tool-augmented LLM reasoning
* Structured output generation
* Self-evaluation via critic agent
* Real-time research automation
* Modular and extensible design

---

## 🧪 Example Workflow

### Input:

```text id="rq7lzw"
"Quantum computing breakthroughs in 2025"
```

### Output:

* Structured research report
* Sources extracted from web
* Critic evaluation (e.g., 8/10)

---

## 🧠 Design Principles

* **Separation of responsibilities** → Each agent has a clear role
* **Tool augmentation** → LLMs enhanced with external capabilities
* **Composable pipelines** → Chains + agents working together
* **Transparency** → Intermediate outputs exposed to user

---

## 🚀 How to Run

```bash id="c0qj6y"
# Install dependencies
pip install -r requirements.txt

# Add environment variables
TAVILY_API_KEY=your_key
OPENAI_API_KEY=your_key

# Run app
streamlit run app.py
```

---

## 📌 Limitations

* Dependent on external APIs (Tavily, OpenAI)
* Scraping may fail for complex websites
* No long-term memory or context retention
* No parallel execution (currently sequential pipeline)

---

## 🔥 Future Improvements

* Add multi-document retrieval (RAG pipeline)
* Introduce vector database (FAISS / Pinecone)
* Enable parallel agent execution
* Add citation verification system
* Deploy as scalable API (FastAPI + Docker)
* Add memory for iterative research

---

## 🧠 Engineering Takeaways

This project demonstrates:

* Multi-agent system design
* LLM orchestration using LangChain
* Tool integration with AI agents
* Prompt engineering for structured outputs
* Building interactive AI applications

---

## ⭐ Why This Project Matters

This system reflects the direction of modern AI systems:

> From single LLM calls → to collaborative AI agent ecosystems

It aligns with how companies like Google, OpenAI, and Anthropic design advanced AI workflows.

---

## 🤝 Contribution

Open to improvements in:

* Agent orchestration
* UI/UX enhancements
* Model optimization

---

## 📄 License

MIT License
