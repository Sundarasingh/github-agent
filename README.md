# Agents with LangGraph

## Project Overview

`agents-with-langgraph` is a Python library that demonstrates how to build modular, AI‑driven agents using **LangChain**, **LangGraph**, and **Groq**. The project showcases a coordinator agent that delegates tasks to specialized sub‑agents for documentation, release notes, issue management, and code review. It serves as a reference implementation for building complex, tool‑enabled AI workflows.

## Features

- **Modular Sub‑Agents**: Separate agents for documentation, release notes, issue handling, and code review.
- **Tool Integration**: Uses LangChain tools to interact with GitHub, environment variables, and other utilities.
- **Graph‑Based Coordination**: Leverages LangGraph for orchestrating multi‑step workflows.
- **Extensible Architecture**: Easily add new agents or tools to extend functionality.

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/agents-with-langgraph.git
   cd agents-with-langgraph
   ```

2. **Create a Virtual Environment** (Python 3.12+ recommended)
   ```bash
   python -m venv .venv
   source .venv/bin/activate   # On Windows: .venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install --upgrade pip
   pip install -e .
   ```
   The `pyproject.toml` defines the required packages, including LangChain, LangGraph, and Groq.

4. **Configure Environment Variables**
   - Copy the example environment file and fill in the required values:
     ```bash
     cp sample.env .env
     ```
   - Edit `.env` and set your Groq API key and any GitHub credentials needed for the toolkit.

5. **Run the Coordinator**
   ```bash
   python -m src.workflow.main
   ```
   This will start the coordinator agent, which can handle documentation updates, release note generation, issue management, and code reviews via sub‑agents.

## Contribution Guidelines

We welcome contributions! Please follow these steps:

1. **Fork the Repository** and create a new branch for your feature or bug fix:
   ```bash
   git checkout -b my-feature-branch
   ```

2. **Make Your Changes** adhering to the existing code style (PEP 8) and add or update tests where applicable.

3. **Run Tests** (if any) and ensure the project builds:
   ```bash
   pytest   # or your preferred test runner
   ```

4. **Update Documentation** if your changes affect usage or APIs. The `documentation_agent` can help generate or refine docs.

5. **Commit and Push** your changes:
   ```bash
   git add .
   git commit -m "Brief description of changes"
   git push origin my-feature-branch
   ```

6. **Open a Pull Request** against the `main` branch. Provide a clear description of what the PR does, reference any related issues, and ensure that all checks pass.

---

*Happy hacking!*