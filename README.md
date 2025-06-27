
# 🤖 BrowserAgent-GPT-Navigator

**BrowserAgent-GPT-Navigator** is a powerful Streamlit-based web application that lets you interact with websites using natural language commands. It combines the flexibility of [Puppeteer](https://pptr.dev/) for browser automation, [OpenAI GPT models](https://platform.openai.com/docs) for intelligent reasoning, and [MCP Agents](https://pypi.org/project/mcp-agent/) to orchestrate modular workflows.

> 🧠 Imagine asking an agent to *"Go to Wikipedia, click on Object Detection, scroll down, and summarize the section."*  
> This project does exactly that.

---

## 🌟 Features

- 🔍 **Natural Language Control**: Just describe what you want the agent to do.
- 🌐 **Web Navigation**: Navigate to URLs, click buttons, follow links, scroll dynamically.
- ✍️ **Content Summarization**: Get clean markdown summaries of webpage sections.
- 📸 **Screenshot Capabilities**: Automatically captures elements or full-page views.
- 🔄 **Multi-step Task Execution**: Supports chained commands for complex workflows.
- 🚀 **Streamlit UI**: Simple, responsive, and interactive frontend.

---

## 📦 Tech Stack

- **[Streamlit](https://streamlit.io/)** – Web interface  
- **[MCP Agent](https://pypi.org/project/mcp-agent/)** – Multi-agent orchestration  
- **[OpenAI API](https://platform.openai.com/)** – LLM reasoning  
- **[Puppeteer](https://pptr.dev/)** – Browser automation  
- **Asyncio** – Async execution  

---

## 🚀 Getting Started

### 🛠️ Prerequisites

- Python 3.8+
- Node.js (required for Puppeteer)
- [OpenAI API Key](https://platform.openai.com/account/api-keys)

---

### 📁 Clone the Repository

```bash
git clone https://github.com/Electrolight123/BrowserAgent-GPT-Navigator.git
cd BrowserAgent-GPT-Navigator
```

---

### ⚙️ Environment Setup with `uv`

`uv` is a modern, fast Python package manager and virtual environment tool.

1. **Install `uv`:**
   ```bash
   pip install uv
   ```

2. **Initialize environment:**
   ```bash
   uv init
   ```

3. **Install dependencies:**
   ```bash
   uv pip install -r requirements.txt
   ```

---

### 🔑 Set Your OpenAI API Key

```bash
export OPENAI_API_KEY=sk-...
```

---

### 🧾 Configuration

Ensure the following in `mcp_agent.config.yaml`:

```yaml
execution_engine: asyncio
logger:
  transports: [console, file]
  level: debug
  progress_display: true
  path_settings:
    path_pattern: "logs/mcp=agent-{unique_id}.jsonl"
    unique_id: "timestamp"
    timestamp_format: "%Y%m%d_%H%M%S"

mcp:
  servers:
    puppeteer:
      command: "npx"
      args: ["-y", "@modelcontextprotocol/server-puppeteer"]

openai:
  default_model: "gpt-4.1-mini-2025-06-25"
```

---

## ▶️ Run the App

```bash
streamlit run main.py
```

---

## 💬 Example Commands

- `Go to wikipedia.org/wiki/computer_vision`
- `Click on the link to object detection and take a screenshot`
- `Scroll down and summarize the page`

---

## 📄 Requirements

Dependencies are listed in [`requirements.txt`](./requirements.txt).  
Regenerate anytime with:

```bash
uv pip freeze > requirements.txt
```

Sample:
```
streamlit>=1.28.0
mcp-agent>=0.0.14
asyncio>=3.4.3
openai>=1.0.0
```

---

## 🛡️ License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgements

- [Streamlit](https://streamlit.io/)
- [OpenAI](https://openai.com/)
- [Puppeteer](https://pptr.dev/)
- [MCP Agent Protocol](https://pypi.org/project/mcp-agent/)

---

## ⭐️ Show Your Support

If you found this helpful:

- ⭐ Star the repo
- 🗣 Share it
- 🤝 Contribute    

