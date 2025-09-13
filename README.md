# 🧞‍♂️ Code Smith Genie 🧞‍♂️

**Code Smith Genie** 🧞 is an AI-powered coding assistant built with [LangGraph](https://github.com/langchain-ai/langgraph).  
It works like a multi-agent development team that can take a natural language request and transform it into a complete, working project — file by file — using real developer workflows.

---

## 🏗️ Architecture

- **Planner Agent** – Analyzes your request and generates a detailed project plan.
- **Architect Agent** – Breaks down the plan into specific engineering tasks with explicit context for each file.
- **Coder Agent** – Implements each task, writes directly into files, and uses available tools like a real developer.

<div style="text-align: center;">
    <img src="resources/coder_buddy_diagram.png" alt="Coder Agent Architecture" width="90%"/>
</div>

---

## 🚀 Getting Started
### Prerequisites
- Make sure you have uv installed, follow the instructions [here](https://docs.astral.sh/uv/getting-started/installation/) to install it.
- Ensure that you have created a groq account and have your API key ready. Create an API key [here](https://console.groq.com/keys).

### ⚙️ **Instsllstion and Startup**
- Create a virtual environment using: `uv venv` and activate it using `source .venv/bin/activate`
- Install the dependencies using: `uv pip install -r pyproject.toml`
- Create a `.env` file and add the variables and their respective values mentioned in the `.sample_env` file

Now that we are done with all the set-up & installation steps we can start the application using the following command:
  ```bash
    python main.py
  ```

### 🧪 Example Prompts
- Create a to-do list application using html, css, and javascript.
- Create a simple calculator web application.
- Create a simple blog API in FastAPI with a SQLite database.

---


## Project Structure

```
coder-buddy/
│
├── main.py                # Entry point for running the agent
├── pyproject.toml         # Project metadata and dependencies
├── uv.lock                # Lock file for dependency management
├── README.md              # Project documentation
├── .env                   # Environment variables (not tracked in git)
├── .gitignore             # Git ignore rules
├── .python-version        # Python version specification
│
├── agent/                 # Core agent logic and modules
│   ├── __init__.py        # Package initializer
│   ├── graph.py           # Agent graph and workflow management
│   ├── prompts.py         # Prompt templates and handling
│   ├── states.py          # Agent state management
│   ├── tools.py           # Tool definitions and integrations
│   └── __pycache__/       # Python bytecode cache
│
├── resources/             # Project resources and diagrams
│   ├── coder_buddy_diagram.mmd   # Mermaid diagram of agent architecture
│   └── coder_buddy_diagram.png   # PNG image of agent architecture
│   └── coder_buddy_diagram.png   # PNG image of agent architecture
│
├── .idea/                 # IDE configuration (for JetBrains IDEs)
│   └── ...                # Various IDE config files
│
└── .venv1/                # Local Python virtual environment
   └── ...                # Python binaries and site-packages
```

### File Descriptions

- **main.py**: Launches the Coder Smith Genie 🧞  agent and handles CLI interactions.
- **pyproject.toml**: Specifies project dependencies and build system.
- **uv.lock**: Dependency lock file for reproducible installs.
- **agent/**:
  - **graph.py**: Manages agent workflow and execution graph.
  - **prompts.py**: Contains prompt templates for agent communication.
  - **states.py**: Handles agent state transitions and persistence.
  - **tools.py**: Defines and integrates tools used by the agent.
- **resources/**:
  - **coder_buddy_diagram.mmd**: Mermaid diagram source for architecture visualization.
  - **coder_buddy_diagram.png**: Rendered architecture diagram.
- **.env**: Stores environment variables (API keys, config).
- **.venv1/**: Python virtual environment for isolated package management.

---

## Setup Instructions

1. **Clone the Repository**
  ```sh
  git clone <your-repo-url>
  cd coder-buddy
  ```

2. **Create and Activate Virtual Environment**
  ```sh
  python3 -m venv .venv1
  source .venv1/bin/activate
  ```

3. **Install Dependencies**
  ```sh
  pip install -r requirements.txt
  # Or, if using pyproject.toml:
  pip install uv
  uv pip install
  ```

4. **Configure Environment Variables**
  - Copy `.env.example` to `.env` and update values as needed.

---

## Running Instructions

1. **Activate the Virtual Environment**
  ```sh
  source .venv1/bin/activate
  ```

2. **Run the Agent**
  ```sh
  python main.py
  ```

3. **(Optional) Customize Agent Behavior**
  - Modify files in `agent/` to add new tools, states, or prompts.

## Additional Notes

- Diagrams in `resources/` help visualize the agent's architecture.
- For development, ensure your Python version matches `.python-version`.

