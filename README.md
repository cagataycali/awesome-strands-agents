# Awesome Strands Agents ✨

> A curated list of awesome resources for [Strands Agents](https://strandsagents.com/) - a model-driven approach to building AI agents in just a few lines of code.

<div align="center">
  <a href="https://strandsagents.com">
    <img src="https://strandsagents.com/latest/assets/logo-auto.svg" alt="Strands Agents" width="150">
  </a>
</div>

---

## Contents

- [What is Strands Agents?](#what-is-strands-agents)
- [Official Resources](#official-resources)
- [Core Components](#core-components)
- [Tools & Extensions](#tools--extensions)
- [Model Providers](#model-providers)
- [Multi-Agent Systems](#multi-agent-systems)
- [Examples & Tutorials](#examples--tutorials)
- [Community Resources](#community-resources)
- [Development Tools](#development-tools)
- [Deployment & Production](#deployment--production)
- [Contributing](#contributing)

---

## What is Strands Agents?

Strands Agents is a simple yet powerful Python SDK that takes a model-driven approach to building and running AI agents. From simple conversational assistants to complex autonomous workflows, from local development to production deployment, Strands Agents scales with your needs.

### Key Features

- 🪶 **Lightweight & Flexible**: Simple agent loop that just works and is fully customizable
- 🧩 **Model Agnostic**: Support for Amazon Bedrock, Anthropic, LiteLLM, Ollama, OpenAI, and custom providers
- 🛠️ **Advanced Capabilities**: Multi-agent systems, autonomous agents, and streaming support
- 🔌 **Built-in MCP**: Native support for Model Context Protocol (MCP) servers
- 🐍 **Python-First**: Easy tool creation using Python decorators
- 🏗️ **Production Ready**: Full observability, tracing, and deployment options

---

## Official Resources

### Documentation
- [Official Documentation](https://strandsagents.com/) - Complete user guide and API reference
- [Quickstart Guide](https://strandsagents.com/latest/user-guide/quickstart/) - Get started in minutes
- [API Reference](https://strandsagents.com/latest/api-reference/agent/) - Complete API documentation
- [Examples](https://strandsagents.com/latest/examples/) - Practical examples and use cases

### Repositories
- [strands-agents/sdk-python](https://github.com/strands-agents/sdk-python) - Core Python SDK
- [strands-agents/tools](https://github.com/strands-agents/tools) - Official tools collection
- [strands-agents/agent-builder](https://github.com/strands-agents/agent-builder) - Interactive agent development toolkit
- [strands-agents/docs](https://github.com/strands-agents/docs) - Documentation source
- [strands-agents/samples](https://github.com/strands-agents/samples) - Sample projects and demos

---

## Core Components

### 📦 Python SDK (`strands-agents`)

The core framework for building AI agents.

```python
from strands import Agent, tool

@tool
def greet(name: str) -> str:
    """Greet someone by name."""
    return f"Hello, {name}!"

agent = Agent(tools=[greet])
agent("Say hello to Alice")
```

**Installation:**
```bash
pip install strands-agents
```

**Key Features:**
- Agent loop management
- Tool execution and registration
- Multiple model provider support
- Streaming and async support
- Context management
- Error handling and retries

### 🔧 Tools Package (`strands-agents-tools`)

A comprehensive collection of pre-built tools for agents.

```python
from strands import Agent
from strands_tools import calculator, file_read, http_request

agent = Agent(tools=[calculator, file_read, http_request])
agent("Calculate the square root of 1764 and save the result to a file")
```

**Installation:**
```bash
pip install strands-agents-tools
```

### 🏗️ Agent Builder (`strands-agents-builder`)

Interactive toolkit for building and testing agents.

```bash
# Install
pipx install strands-agents-builder

# Run interactively
strands

# Build custom tools
strands "Create a tool that analyzes sentiment in text"
```

---

## Tools & Extensions

### 📁 File Operations
- `file_read` - Read files with syntax highlighting and search
- `file_write` - Write content to files with validation
- `editor` - Advanced file editing with line operations and undo

### 🖥️ System & Shell
- `shell` - Execute shell commands with PTY support
- `environment` - Manage environment variables safely
- `python_repl` - Execute Python code with state persistence

### 🌐 Network & APIs
- `http_request` - Make HTTP requests with comprehensive auth
- `slack` - Slack integration with real-time events
- `use_aws` - Direct AWS service integration

### 🧠 AI & Memory
- `memory` - Store and retrieve from Amazon Bedrock Knowledge Bases
- `retrieve` - Semantic search across knowledge bases
- `mem0_memory` - Advanced memory with Mem0 integration
- `think` - Multi-cycle reasoning and analysis

### 🎨 Media & Generation
- `generate_image` - AI image generation with Stable Diffusion
- `nova_reels` - Video generation with Amazon Nova Reel
- `speak` - Text-to-speech with multiple voices
- `image_reader` - Process and analyze images

### 🔄 Multi-Agent & Workflows
- `swarm` - Coordinate multiple agents for parallel processing
- `agent_graph` - Create complex agent relationship graphs
- `workflow` - Define and execute multi-step workflows
- `use_llm` - Create nested AI loops with custom prompts

### 🧮 Utilities
- `calculator` - Advanced mathematical operations with SymPy
- `current_time` - Get current time in any timezone
- `cron` - Schedule recurring tasks
- `journal` - Create structured logs and documentation

---

## Model Providers

### ☁️ Cloud Providers

#### Amazon Bedrock (Default)
```python
from strands import Agent
from strands.models import BedrockModel

model = BedrockModel(
    model_id="us.anthropic.claude-3-7-sonnet-20250219-v1:0",
    temperature=0.3,
    streaming=True
)
agent = Agent(model=model)
```

#### Anthropic
```python
from strands.models.anthropic import AnthropicModel

model = AnthropicModel(
    model_id="claude-3-7-sonnet-20250219",
    api_key="your-api-key"
)
```

#### OpenAI
```python
from strands.models.openai import OpenAIModel

model = OpenAIModel(
    model_id="gpt-4o",
    api_key="your-api-key"
)
```

### 🖥️ Local Providers

#### Ollama
```python
from strands.models.ollama import OllamaModel

model = OllamaModel(
    host="http://localhost:11434",
    model_id="llama3.2"
)
```

### 🔗 Unified Providers

#### LiteLLM
```python
from strands.models.litellm import LiteLLMModel

model = LiteLLMModel(
    model_id="gpt-4o",
    api_key="your-api-key"
)
```

#### LlamaAPI
```python
from strands.models.llamaapi import LlamaAPIModel

model = LlamaAPIModel(
    model_id="llama3.1-405b"
)
```

---

## Multi-Agent Systems

### 🐝 Swarm Intelligence
```python
from strands_tools import swarm

# Collaborative problem solving
result = agent.tool.swarm(
    task="Design a sustainable urban transportation system",
    swarm_size=5,
    coordination_pattern="collaborative"
)
```

### 🕸️ Agent Graphs
```python
from strands_tools import agent_graph

# Create agent network
graph = agent.tool.agent_graph(
    action="create",
    graph_id="analysis_network",
    topology={
        "type": "star",
        "nodes": [
            {"id": "coordinator", "role": "main", "system_prompt": "You coordinate analysis"},
            {"id": "data_analyst", "role": "analyzer", "system_prompt": "You analyze data"},
            {"id": "reporter", "role": "reporter", "system_prompt": "You create reports"}
        ]
    }
)
```

### 🔄 Workflows
```python
from strands_tools import workflow

# Define multi-step workflow
workflow_result = agent.tool.workflow(
    action="create",
    workflow_id="data_pipeline",
    tasks=[
        {"task_id": "fetch", "description": "Fetch data from API"},
        {"task_id": "process", "description": "Process and clean data", "dependencies": ["fetch"]},
        {"task_id": "analyze", "description": "Analyze processed data", "dependencies": ["process"]},
        {"task_id": "report", "description": "Generate final report", "dependencies": ["analyze"]}
    ]
)
```

---

## Examples & Tutorials

### 🚀 Quick Start Examples

#### Simple Agent
```python
from strands import Agent

agent = Agent()
response = agent("Tell me about AI agents")
print(response)
```

#### Agent with Tools
```python
from strands import Agent, tool
from strands_tools import calculator, current_time

@tool
def custom_greeting(name: str, time_of_day: str) -> str:
    """Generate a personalized greeting."""
    return f"Good {time_of_day}, {name}! How can I help you today?"

agent = Agent(tools=[calculator, current_time, custom_greeting])
response = agent("What time is it and calculate 15% tip on $50")
```

#### Memory-Enabled Agent
```python
from strands import Agent
from strands_tools import memory, retrieve

agent = Agent(tools=[memory, retrieve])

# Store information
agent.tool.memory(action="store", content="User prefers morning meetings")

# Later retrieve
response = agent.tool.retrieve(text="meeting preferences")
```

### 🎯 Advanced Examples

#### Web Scraping Agent
```python
from strands import Agent
from strands_tools import http_request, file_write, python_repl

agent = Agent(tools=[http_request, file_write, python_repl])
response = agent("Fetch the latest news from a tech website and summarize the top 3 stories")
```

#### Data Analysis Agent
```python
from strands import Agent
from strands_tools import file_read, python_repl, generate_image

agent = Agent(tools=[file_read, python_repl, generate_image])
response = agent("Analyze the CSV file 'sales_data.csv' and create a visualization")
```

#### DevOps Agent
```python
from strands import Agent
from strands_tools import shell, use_aws, cron, slack

agent = Agent(tools=[shell, use_aws, cron, slack])
response = agent("Check server health, update if needed, and notify the team")
```

---

## Community Resources

### 🎓 Learning Resources
- [Strands Agents Concepts](https://strandsagents.com/latest/user-guide/concepts/) - Core concepts explained
- [Tool Development Guide](https://strandsagents.com/latest/user-guide/concepts/tools/python-tools/) - How to create custom tools
- [Multi-Agent Patterns](https://strandsagents.com/latest/user-guide/concepts/multi-agent/) - Patterns for agent collaboration

### 📚 Example Projects
- **CLI Reference Agent** - Command-line interface implementation
- **Weather Forecaster** - Weather prediction with external APIs
- **Memory Agent** - Persistent memory across conversations
- **File Operations Agent** - Advanced file manipulation
- **Knowledge Base Workflow** - RAG implementation with knowledge bases

### 🔧 Custom Tools
Examples of community-created tools:
- Sentiment analysis tools
- Database connectors
- Social media integrations
- Custom API wrappers

---

## Development Tools

### 🐛 Debugging & Testing
```python
# Enable debug logging
import logging
logging.basicConfig(level=logging.DEBUG)

# Test tools individually
from strands_tools import calculator
result = calculator("2 + 2 * 3")
```

### 📊 Observability
- Built-in OpenTelemetry support
- Langfuse integration for tracing
- Custom metrics and logging
- Performance monitoring

### 🔄 Hot Reloading
```python
# Tools automatically reload during development
from strands_tools import load_tool

# Dynamically load custom tools
agent.tool.load_tool(path="./my_custom_tool.py", name="my_tool")
```

---

## Deployment & Production

### ☁️ AWS Deployment Options
- **AWS Lambda** - Serverless agent deployment
- **AWS Fargate** - Containerized agents
- **Amazon EKS** - Kubernetes-based deployment
- **Amazon EC2** - Traditional server deployment

### 🔧 Configuration Management
```bash
# Environment variables for production
export STRANDS_MODEL_ID="us.anthropic.claude-3-7-sonnet-20250219-v1:0"
export STRANDS_KNOWLEDGE_BASE_ID="your-kb-id"
export BYPASS_TOOL_CONSENT="true"  # For automated environments
export AWS_REGION="us-west-2"
```

### 📈 Scaling Considerations
- Connection pooling for model providers
- Rate limiting and backoff strategies
- Error handling and retry logic
- Resource monitoring and alerts

---

## Contributing

We welcome contributions to the Strands Agents ecosystem! Here's how you can help:

### 🐛 Reporting Issues
- Use the appropriate repository's issue tracker
- Provide detailed reproduction steps
- Include environment information

### 🔧 Contributing Code
1. Fork the relevant repository
2. Create a feature branch
3. Add tests for new functionality
4. Submit a pull request

### 📖 Documentation
- Improve existing documentation
- Add examples and tutorials
- Translate documentation

### 🛠️ Creating Tools
- Build and share custom tools
- Contribute to the official tools collection
- Share integration examples

---

## License

This awesome list is licensed under [CC0 1.0 Universal](LICENSE).

Individual projects maintain their own licenses:
- Strands Agents SDK: [Apache License 2.0](https://github.com/strands-agents/sdk-python/blob/main/LICENSE)
- Strands Tools: [Apache License 2.0](https://github.com/strands-agents/tools/blob/main/LICENSE)
- Agent Builder: [Apache License 2.0](https://github.com/strands-agents/agent-builder/blob/main/LICENSE)

---

## ⚠️ Preview Status

Strands Agents is currently in public preview. During this period:
- APIs may change as the SDK evolves
- We welcome feedback and contributions
- Breaking changes may occur between versions

---

<div align="center">
  <sub>Built with ❤️ by the Strands Agents community</sub>
</div>