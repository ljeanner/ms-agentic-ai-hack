# Unlocking Multi-Agent Capabilities with Azure AI Services

Welcome to the Multi-Agent Insurance Claims Processing Hackathon! Today, you'll explore intelligent agent systems powered by Azure AI to streamline complex insurance workflows. Get ready for a hands-on, high-impact day of learning and innovation!

## Introduction
Get ready to transform insurance with AI! In this hackathon, you'll build intelligent agents that process claims, analyze documents, and make smart decisions—just like real insurance pros. From reading handwritten forms to detecting fraud, your agents will collaborate to handle complex workflows in minutes, not weeks. By the end, you'll have created a powerful multi-agent system that redefines insurance claim processing.

## Learning Objectives

By participating in this hackathon, you will learn how to:
- **Build Intelligent Document Systems** using Azure Document Intelligence and GPT-4.1-mini to extract and analyze data from complex insurance documents.
- **Create and Test AI Agents** with Azure AI Agent Service for automated claim processing.
- **Monitor and Evaluate Agents** using Azure AI Foundry for performance, safety, and reliability.
- **Develop Specialized Agents** (e.g., Policy Checker, Claim Reviewer, Risk Analyzer) with Semantic Kernel.
- **Orchestrate Multi-Agent Systems** using Azure Container Apps and advanced coordination patterns for seamless claims handling.

## Architecture
This solution automates insurance claim processing using a multi-agent AI system on Azure. Claims are uploaded along crash documents to Storage Accounts, triggering workflows that clean and structure data with Azure AI Foundry (GPT-4.1-mini). Structured data is stored in Cosmos DB and indexed with Azure AI Search. If you want to know more about how to automatize this, have a look at [last year's hackathon](https://github.com/martaldsantos/doc-process-hack/tree/main/Challenge4). Then, follows the orchestration of specialized AI agents—a Policy Checker, Claim Reviewer, and Risk Analyser—that collaborate to assess claims, detect fraud, and generate a comprehensive summary for human review. Application Insights and Log Analytics monitors the system for performance and reliability, enabling efficient, accurate, and scalable claim handling.

<img width="1828" height="815" alt="image" src="https://github.com/user-attachments/assets/f776cc4b-90da-4898-8a1c-a96282f39bbc" />

## Requirements
To successfully complete this hackathon, you will need the following:

- GitHub account to access the repository.
- Be familiar with Python programming, including handling JSON data and making API calls.​
- Be familiar with Generative AI Solutions and Azure AI Services.
- An active Azure subscription, with Owner or Contributor rights.
- Ability to provision resources in **Sweden Central** or [another supported region](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/concepts/models?tabs=global-standard%2Cstandard-chat-completions#global-standard-model-availability).

## Local Environment Setup

### Prerequisites
Before starting the workshop, ensure you have the following installed on your local machine:

#### 1. Python
- **Python 3.9 or later** (recommended: Python 3.11)
- Download from [python.org](https://www.python.org/downloads/)
- Verify installation: `python --version` or `python3 --version`

#### 2. Git
- Download from [git-scm.com](https://git-scm.com/downloads)
- Verify installation: `git --version`

#### 3. Code Editor
- **Visual Studio Code** (recommended) with Python extension
- Download from [code.visualstudio.com](https://code.visualstudio.com/)

#### 4. Azure CLI (Optional but recommended)
- Download from [docs.microsoft.com/en-us/cli/azure/install-azure-cli](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)
- Verify installation: `az --version`

### Installation Steps

#### 1. Clone the Repository
```bash
git clone ''
cd agentic-ai-hack
```

#### 2. Create a Python Virtual Environment
```bash
# Windows (PowerShell)
python -m venv venv
.\venv\Scripts\Activate.ps1

# Windows (Command Prompt)
python -m venv venv
venv\Scripts\activate.bat

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

#### 3. Install Dependencies
```bash
# Install main requirements
pip install -r requirements.txt

# For Challenge 5 only (Azure Functions and FastAPI)
cd challenge-5
pip install -r requirements.txt
cd ..
```

#### 4. Install Jupyter Notebook (for interactive challenges)
```bash
pip install jupyter notebook ipykernel
```

#### 5. Verify Installation
```bash
# Test key Python packages
python -c "import azure.ai.projects; print('Azure AI Projects installed successfully')"
python -c "import semantic_kernel; print('Semantic Kernel installed successfully')"
python -c "import jupyter; print('Jupyter installed successfully')"
```

### Key Dependencies
This workshop uses the following main packages:
- **Azure AI Services**: `azure-ai-projects`, `azure-ai-agents`, `azure-ai-formrecognizer`, `azure-ai-evaluation`
- **Azure Core**: `azure-identity`, `azure-cosmos`, `azure-search-documents`, `azure-storage-blob`
- **AI/ML**: `semantic-kernel`, `openai`, `scikit-learn`, `pandas`, `numpy`
- **Development**: `jupyter`, `fastapi`, `uvicorn`, `pytest`
- **Web**: `aiohttp`, `httpx`, `websockets`

### Environment Configuration
Before starting the challenges, you'll need to:
1. Set up Azure resources (see Challenge 0)
2. Configure environment variables for Azure services
3. Obtain API keys and connection strings from Azure Portal

### Troubleshooting

#### Common Issues
- **Permission errors**: Run terminal as administrator (Windows) or use `sudo` (macOS/Linux)
- **Python version issues**: Ensure you're using Python 3.9+
- **Package conflicts**: Use a fresh virtual environment
- **Azure authentication**: Ensure you're logged in to Azure CLI: `az login --use-device-code`

#### Windows Specific
- **PowerShell execution policy**: Run `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser` if you get script execution errors
- **Long path issues**: Enable long paths in Windows if you encounter path length errors

#### Virtual Environment Issues
```bash
# If you need to recreate your virtual environment
deactivate  # if currently activated
rm -rf venv  # or rmdir /s venv on Windows
python -m venv venv
# Reactivate and reinstall requirements
```

### IDE Setup
For Visual Studio Code:
1. Install the Python extension
2. Install the Jupyter extension  
3. Install the Azure extensions (Azure Account, Azure Resources)
4. Select your virtual environment as the Python interpreter (`Ctrl+Shift+P` → "Python: Select Interpreter")
5. Configure workspace settings for better Azure integration

### Running Jupyter Notebooks
```bash
# Start Jupyter notebook server
jupyter notebook

# Or use VS Code's integrated Jupyter support
# Open .ipynb files directly in VS Code
```




## Challenges

- Challenge 00: **[Environment Setup & Azure Resource Deployment](challenge-0/README.md)** : Deploy foundational Azure services and set up your development environment for the hackathon
- Challenge 01: **[Document Processing and Vectorized Search](challenge-1/README.md)**: Build a comprehensive document processing system using multimodal analysis and Azure AI Search for semantic understanding
- Challenge 02: **[Build and Test Your First Agent](challenge-2/README.md)**: Create your first intelligent agent using Azure AI Agent Service to handle insurance claim processing workflows
- Challenge 03: **[Agent Observability and Evaluation](challenge-3/README.md)**: Implement comprehensive observability and evaluation frameworks for your AI agents using Azure AI Foundry's evaluation capabilities
- Challenge 04: **[Semantic Kernel + Azure AI Agent Service Agents](challenge-4/readme.md)**: Create specialized AI agents (Policy Checker, Claim Reviewer, Risk Analyser) using Semantic Kernel integration for enhanced capabilities
- Challenge 05: **[Agent Orchestration](challenge-5/README.md)** Coordinate multiple specialized agents to work together on complex tasks through various orchestration patterns with Azure Container Apps
