# Awesome Agent Infrastructure [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com) [![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

A curated list of infrastructure for building reliable LLM agents — frameworks, memory, tool protocols, sandboxes, browsers, observability, and retrieval.

Maintained by [Backblaze](https://www.backblaze.com).

### Related Lists

- [Awesome ML Data Pipelines](https://github.com/backblaze-labs/awesome-ml-data-pipelines)
- [Awesome Multimodal Data](https://github.com/backblaze-labs/awesome-multimodal-data)
- [Awesome Physical AI](https://github.com/backblaze-labs/awesome-physical-ai)
- [Awesome Image Generation](https://github.com/backblaze-labs/awesome-image-generation)
- [Awesome Video Generation](https://github.com/backblaze-labs/awesome-video-generation)
- [Awesome Audio Generation](https://github.com/backblaze-labs/awesome-audio-generation)

## Contents

- [Agent Frameworks](#agent-frameworks)
- [Memory and State](#memory-and-state)
- [Tool Protocols and Servers](#tool-protocols-and-servers)
- [Execution Sandboxes](#execution-sandboxes)
- [Browser and Computer Use](#browser-and-computer-use)
- [Observability and Evaluation](#observability-and-evaluation)
- [Retrieval and RAG](#retrieval-and-rag)
- [Vector Databases](#vector-databases)
- [Templates and Example Projects](#templates-and-example-projects)

---

## Agent Frameworks

> Libraries for building LLM agents — planning, tool use, multi-agent orchestration.

- **[Microsoft AutoGen](https://microsoft.github.io/autogen/)** – Multi-agent conversation framework from Microsoft Research. AutoGen 0.4 rewrote it around an event-driven runtime. [Docs](https://microsoft.github.io/autogen/stable/) | SDK: Python (pip install autogen-agentchat)
- **[CrewAI](https://www.crewai.com)** – Role-based multi-agent framework. Agents, tasks, and tools composed into crews with deterministic or planning-based flows. [Docs](https://docs.crewai.com) | SDK: Python (pip install crewai)
- **[Agno](https://www.agno.com)** – Lightweight Python framework for building multimodal agents and agentic systems. Formerly Phidata. [Docs](https://docs.agno.com) | SDK: Python (pip install agno)
- **[LangGraph](https://langchain-ai.github.io/langgraph/)** – Graph-based agent runtime from the LangChain team. Durable execution, human-in-the-loop, and multi-actor patterns. [Docs](https://langchain-ai.github.io/langgraph/tutorials/introduction/) | SDK: Python (pip install langgraph), JS (npm install @langchain/langgraph)
- **[HuggingFace smolagents](https://huggingface.co/docs/smolagents)** – Minimal "code agent" library — agents write Python to solve tasks. ~1k LoC core; easy to audit and extend. [Docs](https://github.com/huggingface/smolagents) | SDK: Python (pip install smolagents)
- **[Mastra](https://mastra.ai)** – TypeScript-first agent framework with workflows, RAG, and evals. From the creators of Gatsby. [Docs](https://mastra.ai/docs) | SDK: TypeScript (npm install @mastra/core)
- **[OpenAI Agents SDK](https://openai.github.io/openai-agents-python/)** – Official OpenAI agent framework. Handoffs, guardrails, built-in tracing, and Responses-API-native execution. [Docs](https://github.com/openai/openai-agents-python) | SDK: Python (pip install openai-agents)
- **[Pydantic AI](https://ai.pydantic.dev)** – Agent framework from the Pydantic team. Type-safe tool calling, structured outputs, dependency injection. [Docs](https://ai.pydantic.dev) | SDK: Python (pip install pydantic-ai)
- **[Google ADK](https://adk.dev)** – Google's open-source agent development kit. Build, evaluate, and deploy multi-agent systems; multi-language with Gemini-optimized but model-agnostic. [Docs](https://adk.dev) | SDK: Python (pip install google-adk), TypeScript (npm install @google/adk)
- **[Langroid](https://langroid.github.io/langroid/)** – Lightweight Python multi-agent framework from CMU/UW-Madison. Task-delegation via message passing; no LangChain dependency. [Docs](https://langroid.github.io/langroid/) | SDK: Python (pip install langroid)
- **[Microsoft Agent Framework](https://devblogs.microsoft.com/agent-framework/)** – Microsoft's production-ready open-source agent SDK and runtime for Python and .NET. Unifies AutoGen orchestration and Semantic Kernel foundations. [Docs](https://learn.microsoft.com/en-us/agent-framework/overview/) | SDK: Python (pip install agent-framework), .NET (dotnet add package Microsoft.Agents.AI)

## Memory and State

> Long-term memory, session state, and knowledge-retention layers for agents.

- **[Mem0](https://mem0.ai)** – Memory layer for AI agents. Personalization through user/agent/session memories with semantic recall. [Docs](https://docs.mem0.ai) | SDK: Python (pip install mem0ai), Node (npm install mem0ai)
- **[Letta](https://www.letta.com)** – Open-source agent server focused on long-term memory. Successor to MemGPT; agents are first-class stateful services. [Docs](https://docs.letta.com) | SDK: Python (pip install letta-client)
- **[Zep](https://www.getzep.com)** – Memory and context platform for LLM apps. Knowledge-graph-backed user memory with temporal reasoning. [Docs](https://help.getzep.com)
- **[Graphiti](https://github.com/getzep/graphiti)** – Open-source temporal context graph engine. Tracks how facts change over time with full provenance; hybrid semantic + keyword + graph retrieval. [Docs](https://help.getzep.com/graphiti) | SDK: Python (pip install graphiti-core)

## Tool Protocols and Servers

> Standardised interfaces for exposing tools and data sources to agents (MCP and friends).

- **[MCP Reference Servers](https://github.com/modelcontextprotocol/servers)** – Reference MCP server implementations for filesystem, Git, GitHub, SQL, Slack, and more.
- **[MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk)** – Official Python SDK for building and consuming MCP servers and clients. SDK: Python (pip install mcp)
- **[MCP TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk)** – Official TypeScript SDK for MCP servers and clients. SDK: TypeScript (npm install @modelcontextprotocol/sdk)
- **[Anthropic Model Context Protocol](https://modelcontextprotocol.io)** – Open protocol for connecting AI applications to tools and data sources. Spec, reference servers, and official SDKs. [Docs](https://modelcontextprotocol.io/introduction)
- **[Agent2Agent Protocol (A2A)](https://github.com/a2aproject/A2A)** – Open protocol for communication and interoperability between AI agents. JSON-RPC 2.0 over HTTP with SDKs for Python, Go, JS, Java, and .NET. [Docs](https://a2a-protocol.org)
- **[MCP Inspector](https://github.com/modelcontextprotocol/inspector)** – Interactive visual tool for testing and debugging MCP servers. Supports STDIO, SSE, and Streamable HTTP transports. SDK: TypeScript (npx @modelcontextprotocol/inspector)
- **[MCPX](https://github.com/TheLunarCompany/lunar/tree/main/mcpx)** – Open-source MCP gateway and aggregator. Consolidates multiple MCP servers behind a single governed entry point with rate limiting and traffic policies. [Docs](https://docs.lunar.dev/mcpx/)

## Execution Sandboxes

> Secure environments for running agent-generated code, shell commands, and browser sessions.

- **[Daytona](https://www.daytona.io)** – Open-source dev-environment manager; Daytona Sandboxes expose a sandbox API for agents and CI pipelines. [Docs](https://www.daytona.io/docs)
- **[E2B](https://e2b.dev)** – Secure cloud sandboxes for running AI-generated code. Firecracker microVMs, sub-second startup, per-session isolation. [Docs](https://e2b.dev/docs) | SDK: Python (pip install e2b), JS (npm install @e2b/code-interpreter)
- **[Microsoft Agent Governance Toolkit](https://github.com/microsoft/agent-governance-toolkit)** – Runtime policy enforcement for autonomous agents. Zero-trust identity, execution sandboxing, sub-millisecond policy checks; covers all 10 OWASP Agentic Top 10 risks. SDK: Python (pip install agent-governance-toolkit), TypeScript (npm install @microsoft/agentmesh-sdk)
- **[Modal Sandboxes](https://modal.com/docs/guide/sandbox)** – Serverless sandbox primitive inside Modal. Arbitrary container execution, ephemeral filesystems, strict network policies.
- **[Riza](https://riza.io)** – Secure code-execution API for LLM tool calls. Python, JS, PHP, Ruby; strict WASM-based isolation. [Docs](https://docs.riza.io)

## Browser and Computer Use

> Platforms and SDKs that let agents drive web browsers and full desktops.

- **[browser-use](https://browser-use.com)** – Open-source library giving LLMs reliable control of a Playwright browser. Self-host or use their cloud. [Docs](https://docs.browser-use.com) | SDK: Python (pip install browser-use)
- **[Playwright MCP](https://github.com/microsoft/playwright-mcp)** – Microsoft's official MCP server for Playwright. Gives any MCP-aware agent a controllable browser.
- **[Anthropic Computer Use](https://docs.claude.com/en/docs/build-with-claude/computer-use)** – Claude's computer-use tool for controlling a full desktop. Reference Docker image and sample agent loop from Anthropic.
- **[Browserbase](https://www.browserbase.com)** – Managed headless browsers for AI agents. Session recording, proxying, CAPTCHA handling, and a Stagehand framework. [Docs](https://docs.browserbase.com) | SDK: Python (pip install browserbase), Node (npm install @browserbase/sdk)

## Observability and Evaluation

> Tracing, logging, metrics, and automated evals for LLM applications.

- **[Langfuse](https://langfuse.com)** – Open-source LLM engineering platform — traces, prompt management, datasets, and evals. Self-host or managed. [Docs](https://langfuse.com/docs) | SDK: Python (pip install langfuse), JS (npm install langfuse)
- **[Opik (Comet)](https://www.comet.com/site/products/opik/)** – Open-source LLM evaluation and tracing from Comet. Playground, datasets, experiment comparison. [Docs](https://www.comet.com/docs/opik/) | SDK: Python (pip install opik)
- **[Arize Phoenix](https://phoenix.arize.com)** – Open-source LLM tracing and evaluation. OpenTelemetry-based, self-hostable, integrates with every major framework. [Docs](https://docs.arize.com/phoenix) | SDK: Python (pip install arize-phoenix)
- **[Helicone](https://www.helicone.ai)** – Open-source proxy-based observability for LLM apps. Logging, caching, rate-limiting, and costs with minimal code. [Docs](https://docs.helicone.ai)
- **[LangSmith](https://www.langchain.com/langsmith)** – Commercial tracing, evaluation, and prompt engineering platform from the LangChain team. Works with any LLM framework. [Docs](https://docs.smith.langchain.com)
- **[OpenLLMetry](https://github.com/traceloop/openllmetry)** – OpenTelemetry-based instrumentation for LLM apps. Drop-in tracing for OpenAI, Anthropic, LangChain, LlamaIndex, and major vector DBs. SDK: Python (pip install traceloop-sdk), TypeScript (npm install @traceloop/node-server-sdk)
- **[TruLens](https://github.com/truera/trulens)** – Open-source evaluation and tracking for LLM apps and agents. RAG Triad metrics, feedback functions, and experiment comparison dashboard. [Docs](https://www.trulens.org/docs/) | SDK: Python (pip install trulens)

## Retrieval and RAG

> Retrieval-augmented generation frameworks and document-indexing libraries.

- **[LangChain](https://www.langchain.com)** – LLM composition library. Document loaders, retrievers, and chains form the RAG backbone for many apps. [Docs](https://python.langchain.com) | SDK: Python (pip install langchain), JS (npm install langchain)
- **[LlamaIndex](https://www.llamaindex.ai)** – Data framework for connecting custom data sources to LLMs. Document loaders, indexing, query engines, and agents. [Docs](https://docs.llamaindex.ai) | SDK: Python (pip install llama-index), TypeScript (npm install llamaindex)
- **[Haystack (deepset)](https://haystack.deepset.ai)** – End-to-end NLP framework for building RAG, search, and agent applications. Pipelines compose components. [Docs](https://docs.haystack.deepset.ai) | SDK: Python (pip install haystack-ai)
- **[RAGAS](https://www.ragas.io)** – Framework for evaluating RAG pipelines. Reference-free metrics for faithfulness, answer relevancy, and context precision. [Docs](https://docs.ragas.io) | SDK: Python (pip install ragas)

## Vector Databases

> Vector stores and embedding databases commonly used by agents for semantic recall.

- **[Milvus](https://milvus.io)** – Scalable open-source vector database from Zilliz. Horizontal scale, GPU indexing, LF AI & Data graduated project. [Docs](https://milvus.io/docs)
- **[Qdrant](https://qdrant.tech)** – High-performance vector database in Rust. Strong filter DSL, quantization, and hybrid search. [Docs](https://qdrant.tech/documentation/) | SDK: Python (pip install qdrant-client), JS, Rust, Go
- **[Chroma](https://www.trychroma.com)** – AI-native embeddings database. Popular choice for local/laptop development and quick prototyping. [Docs](https://docs.trychroma.com) | SDK: Python (pip install chromadb), JS (npm install chromadb)
- **[pgvector](https://github.com/pgvector/pgvector)** – Open-source vector similarity extension for Postgres. Exact and approximate nearest-neighbour with HNSW and IVFFlat.
- **[Weaviate](https://weaviate.io)** – Vector search with built-in vectorization modules and a schema-aware GraphQL API. [Docs](https://weaviate.io/developer/)
- **[LanceDB](https://lancedb.com)** – Serverless vector database on the Lance columnar format. Zero-copy, versioned, runs directly over S3-compatible storage. [Docs](https://lancedb.github.io/lancedb/) | SDK: Python (pip install lancedb), Rust, Node

## Templates and Example Projects

> Reference implementations, demos, and starter projects.

- **[Awesome MCP Servers](https://github.com/punkpeye/awesome-mcp-servers)** – Community-maintained catalogue of MCP servers. Useful reference when deciding what to build vs. adopt.
- **[LangGraph Examples](https://github.com/langchain-ai/langgraph/tree/main/examples)** – Reference LangGraph flows — ReAct agents, human-in-the-loop, multi-agent collaboration.
- **[OpenAI Agents Python Examples](https://github.com/openai/openai-agents-python/tree/main/examples)** – Official examples for the OpenAI Agents SDK — handoffs, voice, parallelism, guardrails.

---

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md). One entry per PR — edit `entries.yaml` only and let the maintainers regenerate `README.md`.

## License

Released under [CC0 1.0 Universal](LICENSE). You may copy, modify, and redistribute without attribution.

## About Backblaze B2

[Backblaze B2 Cloud Storage](https://www.backblaze.com/cloud-storage) is S3-compatible object storage designed for AI and media workloads. This list is maintained as part of our work making B2 a convenient storage layer for AI workflows.
