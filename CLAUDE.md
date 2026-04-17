# CLAUDE.md — awesome-agent-infrastructure

## What this list is

A curated directory of infrastructure for running LLM agents in production — frameworks, memory, MCP, sandboxes, browser/computer use, observability, retrieval, and vector stores.

## Scope

**Include**
- Agent frameworks (LangGraph, AutoGen, CrewAI, OpenAI Agents SDK, etc.).
- Long-term memory and session-state layers.
- Tool protocols — MCP spec, official SDKs, reference servers.
- Execution sandboxes for running agent-generated code.
- Browser and full computer-use platforms.
- LLM observability, tracing, and evaluation tools.
- RAG frameworks and retrieval libraries.
- Vector databases commonly used by agents.
- Template/demo projects.

**Exclude**
- Base LLM providers (those are not agent infra).
- Pure orchestrators aimed at non-agent ML pipelines — see `awesome-ml-data-pipelines`.
- Research-only agents without usable code.
- Forks or wrappers that don't add meaningful capability.

**Inclusion requirements (every entry)**
- Public product or docs page; URL resolves.
- Activity signal within the last 12 months.
- Open source or a clear developer-access path.

## Files, schema, workflow, rules

Identical to the rest of the awesome-* family. See `~/awesome-lists/CLAUDE.md` for the global workflow and `~/awesome-lists/_shared/schema.json` for field definitions.

Per-repo reminders:

- Edit `entries.yaml` only. `README.md` and `llms.txt` are generated.
- `b2_integration` is a URL to B2 docs, or `""` if none.
- Never delete an entry; tag `needs-review` and log a note in `~/awesome-lists/_tasks/`.
