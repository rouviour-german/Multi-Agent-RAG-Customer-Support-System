# 🤖 Multi-Agent RAG Customer Support System

A state-of-the-art Multi-Agent Retrieval-Augmented Generation (RAG) system designed for sophisticated customer support automation. Built with **Python**, **LangChain**, and **LangGraph**, this system orchestrates specialized AI agents to handle complex, multi-domain travel queries.

---

## 🏗️ System Architecture

The system utilizes a hierarchical multi-agent design, managed as a sophisticated state graph via **LangGraph**.

### 🧩 Core Agents
- **Primary Assistant**: The intelligent dispatcher routing queries to domain experts.
- **Support Experts**:
    - ✈️ **Flight Booking**: Specialized in aviation routes and ticketing.
    - 🚗 **Car Rental**: Expert in vehicle logistics and reservations.
    - 🏨 **Hotel Booking**: Dedicated to accommodation management.
    - 🗺️ **Excursion Expert**: Handles personalized travel recommendations.

### 🛡️ Safety & Reliability
- **Dual-Layer Tooling**: Segregation of `safe` (read) and `sensitive` (write) operations.
- **Human-in-the-Loop**: Mandatory user confirmation for all financial or data-altering actions.
- **Memory Stack**: Persistent session state with chronological check-pointing.

---

## 📊 Orchestration Graph

![Architecture Graph](./graphs/multi-agent-rag-system-graph.png)

---

## 🌐 Enterprise Architecture (AWS)

Designed for massive scale and high availability, leveraging a modern cloud-native stack.

![AWS Architecture](./images/multi_agent_rag_system_architecture_aws.png)

---

## 🛠️ Tech Stack & Observability

- **Core**: Python 3.12, LangChain, LangGraph.
- **Search**: DuckDuckGo, Qdrant Vector Database.
- **Instrumentation**: LangSmith for deep request tracing and performance monitoring.

---

## 🚀 Quick Start

### 1. Installation
```bash
git clone https://github.com/rouviour-german/Multi-Agent-RAG-Customer-Support-System
cd multi-agent-customer-support
poetry install
```

### 2. Configuration
Create a `.env` file with:
- `OPENAI_API_KEY`
- `LANGCHAIN_API_KEY` (Optional for tracing)

### 3. Execution
```bash
# Start vector database
docker compose up qdrant -d

# Generate embeddings
poetry run python vectorizer/app/main.py

# Launch support system
poetry run python customer_support_chat/app/main.py
```

---

## 📽️ Demonstration

![LangSmith Demo](./images/langsmith.gif)
[Watch the full demonstration video here](https://youtu.be/mPBYvSJuN8Q?si=TGmtyp-XK5O5xQV7)

---

## 📄 License

This project is licensed under the MIT License.

---

## Author & Contact

- **GitHub:** [@rouviour-german](https://github.com/rouviour-german)
- **Email:** [rouviourgermanmeetings@gmail.com](mailto:rouviourgermanmeetings@gmail.com)
- **Profile:** https://github.com/rouviour-german

