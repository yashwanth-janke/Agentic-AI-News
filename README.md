# Agentic AI News & Chatbot Platform

A modular, agentic AI platform built with LangGraph, LangChain, and Streamlit. It enables users to interact with advanced chatbots, leverage web search tools, and generate AI news summaries (daily, weekly, monthly) using stateful agentic graphs.

---

## Features

- **Multiple Use Cases**:
  - **Basic Chatbot**: Simple conversational AI.
  - **Chatbot With Web**: Enhanced chatbot with real-time web search capabilities.
  - **AI News Explorer**: Fetches, summarizes, and saves the latest AI news (daily, weekly, monthly).

- **Stateful Agentic Graphs**: Built using LangGraph for flexible, modular workflows.
- **LLM Integration**: Supports Groq LLMs (Llama 3, Gemma 2).
- **Web UI**: Intuitive Streamlit interface for configuration and interaction.
- **API Key Management**: Securely input and manage API keys for Groq and Tavily.

---

## Project Structure

```
app.py
requirements.txt
AINews/
    daily_summary.md
    weekly_summary.md
    monthly_summary.md
src/
    langgraphagenticai/
        main.py
        LLMS/
            groqllm.py
        graph/
            graph_builder.py
        nodes/
            ai_news_node.py
            basic_chatbot_node.py
            chatbot_with_Tool_node.py
        state/
            state.py
        tools/
            search_tool.py
        ui/
            uiconfigfile.py
            uiconfigfile.ini
            streamlitui/
                loadui.py
                display_result.py
```

---

## Getting Started

### 1. Clone the Repository

```sh
git clone <repo-url>
cd Agentic-AI-News
```

### 2. Install Dependencies

```sh
pip install -r requirements.txt
```

### 3. Obtain API Keys

- **Groq API Key**: [Get from Groq Console](https://console.groq.com/keys)
- **Tavily API Key** (for AI News & Web Search): [Get from Tavily](https://app.tavily.com/home)

### 4. Run the Application

```sh
streamlit run app.py
```

---

## Usage

1. **Select LLM**: Choose Groq and the desired model (Llama 3, Gemma 2).
2. **Enter API Keys**: Input your Groq and Tavily API keys in the sidebar.
3. **Choose Use Case**:
   - **Basic Chatbot**: Chat with a simple LLM.
   - **Chatbot With Web**: Chat with web search capabilities.
   - **AI News**: Select a time frame (daily, weekly, monthly) to fetch and summarize AI news.
4. **Interact**: Enter your message or select a time frame to fetch news. Summaries are saved in the `AINews/` directory.

---

## Configuration

- **UI & Options**: Controlled via `src/langgraphagenticai/ui/uiconfigfile.ini`
- **Add/Modify Use Cases**: Extend `graph_builder.py` and add new nodes in `nodes/`.

---

## Requirements

- Python 3.8+
- See `requirements.txt` for all dependencies:
  - langchain, langgraph, langchain_community, langchain_core, langchain_groq, langchain_openai, faiss-cpu, streamlit, tavily-python

---

## File Outputs

- **AI News Summaries**: Saved as markdown files in `AINews/` (e.g., `daily_summary.md`).

---

## License

This project is licensed under the terms of the LICENSE file.

---

## Acknowledgements

- [LangChain](https://github.com/langchain-ai/langchain)
- [LangGraph](https://github.com/langchain-ai/langgraph)
- [Streamlit](https://streamlit.io/)
- [Groq](https://console.groq.com/)
- [Tavily](https://app.tavily.com/)

---