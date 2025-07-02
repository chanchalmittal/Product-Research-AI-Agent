# Patent Innovation Predictor

A powerful agentic AI system for patent trend analysis and future technology prediction, leveraging Ollama, OpenSearch, and CrewAI.

---

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange.svg)
![License](https://img.shields.io/github/license/chanchalmittal/Product-Research-AI-Agent)

## Overview

Patent Innovation Predictor analyzes patent data to identify trends and forecast future innovations in specific technology areas (with a focus on lithium battery technology). It uses a multi-agent architecture combining semantic, hybrid, and iterative search strategies, built on top of Ollama LLM models and OpenSearch.

---

## System Architecture

```
┌───────────────────────────────────────────────────────────────┐
│                     User Interface Layer                      │
└───────────────────────────────────────────────────────────────┘
                │                │                │
                ▼                ▼                ▼
┌───────────────────────────────────────────────────────────────┐
│                     Agent Orchestration Layer                 │
│  ┌──────────────────┐   ┌────────────────┐  ┌───────────────┐ │
│  │ Research Director│   │Patent Retriever│  │Data Analyst   │ │
│  └──────────────────┘   └────────────────┘  └───────────────┘ │
│                                                               │
│  ┌──────────────────┐                                         │
│  │Innovation        │                                         │
│  │Forecaster        │                                         │
│  └──────────────────┘                                         │
└───────────────────────────────────────────────────────────────┘
                │                │                │
                ▼                ▼                ▼
┌───────────────────────────────────────────────────────────────┐
│                   Knowledge Processing Layer                  │
│  ┌───────────────┐    ┌───────────────┐    ┌───────────────┐  │
│  │ Semantic      │    │ Hybrid        │    │ Iterative     │  │
│  │ Search        │    │ Search        │    │ Search        │  │
│  └───────────────┘    └───────────────┘    └───────────────┘  │
└───────────────────────────────────────────────────────────────┘
                │                │                │
                ▼                ▼                ▼
┌───────────────────────────────────────────────────────────────┐
│                        Data Storage Layer                     │
│  ┌───────────────────────────────────────────────────────────┐│
│  │                       OpenSearch                          ││
│  └───────────────────────────────────────────────────────────┘│
└───────────────────────────────────────────────────────────────┘
```

---

## Features

- Multi-agent workflow for advanced patent analysis
- Semantic, hybrid, and iterative search strategies
- Trend and innovation forecasting
- Modular and extendable architecture

---

## Prerequisites

- Python 3.10+
- [Ollama](https://ollama.com/) (for running local LLM models)
- [OpenSearch](https://opensearch.org/) (default: localhost:9200)
- Access to patent data (pre-loaded in OpenSearch)

---

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/chanchalmittal/Product-Research-AI-Agent.git
   cd Product-Research-AI-Agent
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Install and start Ollama:**
   [Follow official Ollama install guide](https://ollama.com/download)
   ```bash
   ollama serve
   ```

5. **Pull required models:**
   ```bash
   ollama pull llama2  # For general agent tasks
   ollama pull nomic-embed-text  # For embeddings
   ```

6. **Start OpenSearch:**
   Make sure your OpenSearch instance is running on `localhost:9200` (or update connection settings in the code).

---

## Configuration

- **Environment variables:** Create a `.env` file for API keys or config (optional)
  ```env
  # Optional API keys
  SERPAPI_API_KEY=your_key_here
  ```
- **OpenSearch setup:** The system will auto-create indices if missing.

---

## Usage

Run the main application:

```bash
python agentic_rag.py
```

You’ll see a menu with options:

1. **Run complete patent trend analysis and forecasting**
   - Executes full multi-agent workflow, saves results to a text file
2. **Search for specific patents**
   - Keyword, semantic, or hybrid search
3. **Iterative patent exploration**
   - Refines search queries, discovers related patents
4. **View system status**
   - Checks OpenSearch & Ollama connectivity, model availability

---

## Example Workflow

1. Start the application
2. Choose option 4 to verify system status
3. Choose option 1 for complete analysis
4. Enter research area (e.g., "Lithium Battery")
5. Select an available Ollama model (e.g., "llama2")
6. Review and save the analysis results

---

## Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## Acknowledgements

- Built with [Ollama](https://ollama.com/), [OpenSearch](https://opensearch.org/), [CrewAI](https://github.com/joaomdmoura/crewAI)
- Patent data sources as appropriate
