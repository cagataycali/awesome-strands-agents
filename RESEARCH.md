# RESEARCH.md — Strands Agents Ecosystem Scan

**Date:** March 26, 2026  
**Method:** GitHub GraphQL API — `topic:strands-agents`, `strands-agents in:name,description`, `strands_agents OR strands-agent in:name,description,readme`  
**Total repos found:** 177 (topic) + 893 (name/desc) + 5,170 (broad readme search) → ~200 unique after dedup

---

## Summary Statistics

| Metric | Value |
|--------|-------|
| Total unique repos with `strands-agents` topic | **177** |
| Total repos mentioning strands-agents in name/desc | **893** |
| Official org repos (strands-agents/*) | **9** |
| strands-labs/* repos | **3** |
| aws-samples/* repos | **30+** |
| Community projects (non-AWS, non-official) | **100+** |
| Already in awesome-strands-agents | **~80** |
| **New/missing from awesome list** | **~30+** |

---

## Official Ecosystem (strands-agents org)

| Repo | ⭐ | Description |
|------|-----|-------------|
| [sdk-python](https://github.com/strands-agents/sdk-python) | 5,375 | Core Python SDK |
| [tools](https://github.com/strands-agents/tools) | 988 | Official tool library |
| [agent-sop](https://github.com/strands-agents/agent-sop) | 853 | Natural language workflows (SOPs) |
| [samples](https://github.com/strands-agents/samples) | 705 | Sample projects |
| [sdk-typescript](https://github.com/strands-agents/sdk-typescript) | 544 | TypeScript SDK |
| [agent-builder](https://github.com/strands-agents/agent-builder) | 396 | Interactive agent builder |
| [mcp-server](https://github.com/strands-agents/mcp-server) | 268 | MCP docs server for coding assistants |
| [docs](https://github.com/strands-agents/docs) | 177 | Documentation source |
| [evals](https://github.com/strands-agents/evals) | 92 | Evaluation framework |
| [devtools](https://github.com/strands-agents/devtools) | 7 | CI/CD shared tooling |

## strands-labs Ecosystem

| Repo | ⭐ | Description |
|------|-----|-------------|
| [ai-functions](https://github.com/strands-labs/ai-functions) | 238 | AI-powered Python functions with runtime post-conditions |
| [robots](https://github.com/strands-labs/robots) | 36 | Robot control with natural language |
| [robots-sim](https://github.com/strands-labs/robots-sim) | 25 | Simulated environments for robot eval |

---

## 🆕 Projects NOT in awesome-strands-agents (Candidates for Addition)

### High Priority (>10 ⭐, active, not in list)

| Repo | ⭐ | Language | Description | Category |
|------|-----|----------|-------------|----------|
| [horizon-rl/strands-sglang](https://github.com/horizon-rl/strands-sglang) | 51 | Python | SGLang model provider for on-policy agentic RL training | Model Providers |
| [horizon-rl/strands-env](https://github.com/horizon-rl/strands-env) | 43 | Python | Environment infrastructure — step, observe, reward for agentic RL | Integration |
| [mikegc-aws/async-agentic-tools](https://github.com/mikegc-aws/async-agentic-tools) | 36 | Python | True async tools — model keeps talking while tools run in background | Developer Tools |
| [strands-labs/ai-functions](https://github.com/strands-labs/ai-functions) | 238 | Python | AI-powered Python functions with runtime post-conditions | Developer Tools |
| [strands-labs/robots-sim](https://github.com/strands-labs/robots-sim) | 25 | Python | Simulated environments for robot agent eval & RL | Robotics |
| [deeheber/job-search-agent](https://github.com/deeheber/job-search-agent) | 13 | Python | Job hunt agent deployed to AgentCore | Enterprise Apps |
| [aws-samples/sample-agentic-chatbot-accelerator](https://github.com/aws-samples/sample-agentic-chatbot-accelerator) | 12 | TypeScript | IaC chatbot accelerator on Strands + AgentCore | Enterprise Apps |
| [aws-samples/sample-badgers](https://github.com/aws-samples/sample-badgers) | 12 | Python | AI document analysis with Gestalt-informed vision prompts | Enterprise Apps |
| [aws-samples/sample-nova-sonic-websocket-agentcore](https://github.com/aws-samples/sample-nova-sonic-websocket-agentcore) | 9 | TypeScript | Real-time voice AI with Nova Sonic + AgentCore | Voice/Audio |
| [aws-samples/sample-strands-chaos-engineering-agents](https://github.com/aws-samples/sample-strands-chaos-engineering-agents) | 11 | Python | Chaos engineering agents | DevOps & Operations |
| [temporal-community/bedrock-agents-mcp-workshop](https://github.com/temporal-community/bedrock-agents-mcp-workshop) | 15 | Python | Temporal + Strands + MCP workshop | Learning Resources |

### Medium Priority (3-10 ⭐, active)

| Repo | ⭐ | Language | Description | Category |
|------|-----|----------|-------------|----------|
| [strands-compose/sdk-python](https://github.com/strands-compose/sdk-python) | 3 | Python | Zero-code YAML-driven agent orchestration | Developer Tools |
| [peitaosu/strands-rs](https://github.com/peitaosu/strands-rs) | 3 | Rust | Strands Agents in Rust (2nd Rust impl) | SDK Implementations |
| [amazon-nova-api/strands-nova](https://github.com/amazon-nova-api/strands-nova) | 4 | Python | Amazon Nova API model provider | Model Providers |
| [lekhnath/strands-redis-session-manager](https://github.com/lekhnath/strands-redis-session-manager) | 6 | Python | Redis-based session management | Integration |
| [Moonlight-CL/AgentX](https://github.com/Moonlight-CL/AgentX) | 10 | Python | Agent runtime implementation | Developer Tools |
| [jztan/blueclaw](https://github.com/jztan/blueclaw) | 2 | Python | Observable agent runtime with execution tracing | Observability |
| [Vivek0712/clawskills-strands](https://github.com/Vivek0712/clawskills-strands) | 7 | Python | Convert OpenClaw skills to Strands tools | Developer Tools |
| [deeheber/strands-agent-template](https://github.com/deeheber/strands-agent-template) | 8 | TypeScript | Boilerplate template for Strands agents | Developer Tools |
| [Anya2089/Airline-booking-demo-strandsagent-agentcore-ver2.0](https://github.com/Anya2089/Airline-booking-demo-strandsagent-agentcore-ver2.0-withsolutionmanager) | 4 | Python | Airline agent v2 with dual memory + solutions manager | Enterprise Apps |
| [elizabethfuentes12/meta-ai-agent-sample-for-aws-agentcore](https://github.com/elizabethfuentes12/meta-ai-agent-sample-for-aws-agentcore) | 3 | Swift | Voice AI agent for Ray-Ban Meta glasses | Voice/Audio |
| [themreza/Metacontext](https://github.com/themreza/Metacontext) | 2 | — | Multi-agent knowledge centralization system | Context Engineering |
| [Anya2089/swarm_multi_agent_with_StrandsAgent](https://github.com/Anya2089/swarm_multi_agent_with_StrandsAgent) | 2 | Python | Swarm multi-agent demo with anti-ping-pong mechanism | Multi-Agent |
| [Anya2089/Weather_Report_Agent_with_Agentboard_Eval](https://github.com/Anya2089/Weather_Report_Agent_with_Agentboard_Eval) | 2 | Python | Weather agent with AgentBoard evaluation | Examples |
| [valyuAI/valyu-agentcore](https://github.com/valyuAI/valyu-agentcore) | 4 | Python | Valyu search tools for AgentCore | Tools & Integration |
| [lemopian/strands-deep-agents](https://github.com/lemopian/strands-deep-agents) | 5 | Python | DeepAgents pattern — planning + sub-agent delegation | Multi-Agent |
| [erwan-simon/datalfred](https://github.com/erwan-simon/datalfred) | 1 | Python | AI chatbot for data lake on Slack | Enterprise Apps |
| [Tarique-B-DevOps/Agentic-Kubernetes-CLI](https://github.com/Tarique-B-DevOps/Agentic-Kubernetes-CLI) | 1 | Python | Natural language → kubectl commands | DevOps & Operations |
| [04bhavyaa/intelligent-work-allocation](https://github.com/04bhavyaa/intelligent-work-allocation) | 2 | Jupyter | Multi-agent work allocation with AI scoring | Enterprise Apps |
| [jztan/strands-agents-learning](https://github.com/jztan/strands-agents-learning) | 2 | Jupyter | Hands-on tutorials from chatbots to multi-agent | Learning Resources |
| [oteroantoniogom/JUANAN](https://github.com/oteroantoniogom/JUANAN) | 1 | Python | Swarm of agents for MRI tumor detection | Healthcare |

### AWS Samples Not in List

| Repo | ⭐ | Description |
|------|-----|-------------|
| [sample-agentic-chatbot-accelerator](https://github.com/aws-samples/sample-agentic-chatbot-accelerator) | 12 | IaC chatbot on Strands + AgentCore |
| [sample-badgers](https://github.com/aws-samples/sample-badgers) | 12 | Document analysis with Gestalt prompts |
| [sample-nova-sonic-websocket-agentcore](https://github.com/aws-samples/sample-nova-sonic-websocket-agentcore) | 9 | Voice AI with Nova Sonic |
| [sample-strands-chaos-engineering-agents](https://github.com/aws-samples/sample-strands-chaos-engineering-agents) | 11 | Chaos engineering agents |
| [sample-agentcore-rai-strands-agents](https://github.com/aws-samples/sample-agentcore-rai-strands-agents) | 5 | Responsible AI with AgentCore |
| [sample-why-agents-fail](https://github.com/aws-samples/sample-why-agents-fail) | 6 | Anti-hallucination: Graph-RAG, guardrails, DebounceHook |
| [sample-aws-idp-pipeline](https://github.com/aws-samples/sample-aws-idp-pipeline) | 13 | IDP pipeline with LanceDB + Step Functions |
| [sample-nova-sonic-speech2speech-webrtc](https://github.com/aws-samples/sample-nova-sonic-speech2speech-webrtc) | 14 | Speech-to-speech via WebRTC |
| [sample-strands-in-5-minutes](https://github.com/aws-samples/sample-strands-in-5-minutes) | 22 | "5 minutes to Strands" Chinese tutorial |
| [sample-strands-agent-with-agentcore](https://github.com/aws-samples/sample-strands-agent-with-agentcore) | 126 | Strands + AgentCore quickstart |

---

## Ecosystem by Category

### Model Providers (6)
- strands-mlx (Apple Silicon) ✅ in list
- strands-cosmos (NVIDIA Cosmos VLM) ✅ just added
- strands-microgpt (pure-Python GPT) ✅ just added
- **strands-sglang** (SGLang for RL) 🆕
- **strands-nova** (Amazon Nova API) 🆕
- strands-nvidia-nim ✅ in list
- strands-clova ✅ in list

### Reinforcement Learning (2) — NEW CATEGORY
- **horizon-rl/strands-sglang** — SGLang provider for on-policy agentic RL 🆕
- **horizon-rl/strands-env** — Gym-like environments for agent RL 🆕

### SDK Implementations (3)
- chaynabors/strands-rs (Rust) ✅ in list
- **peitaosu/strands-rs** (Rust, alternative impl) 🆕
- strands-agents/sdk-typescript ✅ in list

### Session Managers (3)
- afarntrog/strands-sqlite-session-manager ✅ in list
- **lekhnath/strands-redis-session-manager** 🆕
- strands-supabase-session-manager (private)

### Orchestration (2)
- **strands-compose/sdk-python** — YAML-driven agent orchestration 🆕
- **lemopian/strands-deep-agents** — DeepAgents pattern 🆕

---

## Growth Trends

- **177 repos** with `strands-agents` GitHub topic (up from ~80 in mid-2025)
- **5,375 ⭐** on sdk-python (flagship)
- **conda-forge** packages now exist (strands-agents, strands-agents-tools, strands-agents-mcp-server)
- **Horizon RL** (horizon-rl) is building agentic RL infrastructure on Strands — emerging category
- **i18n expansion**: Chinese (mutli-agents, strands-in-5-minutes), Korean (kyopark2014), Spanish (czam01, crhsdc)
- **Ray-Ban Meta glasses** integration shows wearable/AR agents emerging

---

## Key Observations

1. **RL on Strands is emerging** — horizon-rl is building SGLang provider + gym-like environments. This is a new frontier not yet reflected in awesome list.

2. **async-agentic-tools** by mikegc-aws (36⭐) is notable — lets the model keep talking while tools run in background. Not in awesome list.

3. **strands-labs/ai-functions** (238⭐) is surprisingly not in the awesome list despite being a strands-labs official project.

4. **AWS samples explosion** — 30+ aws-samples repos now use Strands, many not tracked. Key missing: chaos engineering, why-agents-fail, Nova Sonic voice, IDP pipeline.

5. **Template/boilerplate repos** emerging (deeheber/strands-agent-template) — ecosystem is maturing.

6. **Healthcare entering** — JUANAN (MRI tumor detection swarm), life-science research assistant.

7. **strands-compose** represents a low-code YAML approach — could be significant for non-developer adoption.

---

*Research conducted by DevDuck on March 26, 2026. Data from GitHub GraphQL API.*
