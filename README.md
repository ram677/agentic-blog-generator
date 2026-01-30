# 🚀 Agentic Blog Generator

An **Agentic AI–powered automated blog generation system** that creates high-quality blogs from a **topic** and optionally translates them into **multiple languages**, using **LangGraph-based agent workflows**, **Groq LLMs**, and **FastAPI**.

The system supports **multi-step reasoning**, **conditional routing**, and **observable agent execution** via LangGraph Studio and LangSmith.

---

## ✨ Key Features

- 🧠 **Agentic AI Workflow** using LangGraph  
- ✍️ **Automatic Blog Title & Content Generation**  
- 🌍 **Multi-language Blog Generation** (English, Hindi, French)  
- 🔀 **Conditional Routing** based on language input  
- 🔎 **Agent Monitoring & Tracing** with LangGraph Studio & LangSmith  
- ⚡ **FastAPI Backend** for easy integration  
- 🤖 **Groq LLM (LLaMA 3.1)** for fast inference  

---

## 🧩 Tech Stack

- **Backend:** FastAPI  
- **Agent Framework:** LangGraph  
- **LLM Orchestration:** LangChain  
- **LLM Provider:** Groq (LLaMA 3.1)  
- **Monitoring & Tracing:** LangSmith  
- **Language:** Python  

---

## 📂 Project Structure

```
agentic-blog-generator/
│
├── src/
│   ├── graphs/          # LangGraph graph definitions
│   ├── nodes/           # Agent nodes (title, content, translation)
│   ├── states/          # Blog state schemas
│   └── llms/            # Groq LLM wrapper
│
├── app.py               # FastAPI application
├── langgraph.json       # LangGraph Studio config
├── request.json         # Sample API request
├── requirements.txt
├── .gitignore
└── README.md
```

---

## ⚙️ Installation & Setup

### 1️⃣ Create a virtual environment
```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
```

### 2️⃣ Install dependencies
```bash
pip install -r requirements.txt
```

---

## 🔐 Environment Variables

Create a `.env` file in the root directory:

```env
GROQ_API_KEY=your_groq_api_key
LANGCHAIN_API_KEY=your_langchain_api_key
LANGSMITH_API_KEY=your_langsmith_api_key
```

> ⚠️ `.env` is ignored via `.gitignore` for security.

---

## ▶️ Running the Application

```bash
uvicorn app:app --reload
```

Server runs at:
```
http://127.0.0.1:8000
```

---

## 🧪 API Usage

### Endpoint
```
POST /blogs
```

### Request (Topic Only)
```json
{
  "topic": "Agentic AI"
}
```

### Request (Topic + Language)
```json
{
  "topic": "Agentic AI",
  "language": "french"
}
```

### Response
```json
{
  "data": {
    "blog": {
      "title": "...",
      "content": "..."
    }
  }
}
```

---

## 🔍 LangGraph Studio & LangSmith

Run the LangGraph development server:

```bash
langgraph dev
```

This enables:
- Graph visualization  
- Step-by-step agent execution  
- State inspection  
- Workflow tracing via LangSmith  

---

## 🎯 Use Cases

- Automated blog platforms  
- Content marketing automation  
- Multi-language publishing systems  
- SEO-driven content pipelines  
- Agentic AI experimentation  

---

## ⭐ Final Note

This project demonstrates **real-world Agentic AI engineering** using **LangGraph**, **conditional routing**, and **observable LLM workflows**, making it well-suited for **GenAI and Agentic AI roles**.
