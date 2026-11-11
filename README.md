# Dynamic MCP Agent

demonstrating an MCP agent that discovers and selects tools using hybrid semantic and keyword search, executes them with LangGraph, and answers questions over documents using RAG.

## Requirements

- Python 3.11 or later
- [uv](https://docs.astral.sh/uv/)
- Node.js
- Gemini and Postman API keys

## Run

Install the project and notebook dependencies:

```bash
uv sync --group dev
```

Create a `.env` file in the project root:

```env
GEMINI_API_KEY=your-gemini-api-key
POSTMAN_API_KEY=your-postman-api-key
```

Start JupyterLab and open the notebook:

```bash
uv run jupyter lab src/mcp_agent/dynamic_mcp_agent.ipynb
```

Set `DOC_PATHS` in the notebook to the documents you want to search, then run its cells in order. The notebook stores its local Qdrant indexes under `src/mcp_agent/qdrant_data/`.
