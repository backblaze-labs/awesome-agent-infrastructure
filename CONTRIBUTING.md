# Contributing

Thanks for your interest in contributing. This list covers infrastructure for running LLM agents in production.

## How to contribute

1. Fork this repo.
2. Edit **`entries.yaml`** only. Do not edit `README.md` or `llms.txt` — those are regenerated.
3. Place your entry in the appropriate category (see `categories.yaml`).
4. Open a PR. One entry per PR.

## What belongs in the list

**We accept**
- Agent frameworks and multi-agent orchestrators.
- Memory, state, and knowledge-retention layers.
- Tool protocols (MCP and friends) plus SDKs and reference servers.
- Execution sandboxes, browser automation, and computer-use platforms.
- Observability, tracing, and evaluation tools.
- RAG frameworks and vector databases.

**We don't accept**
- Base LLM providers.
- Tools that duplicate an existing entry without clear differentiation.
- Research-only agents without usable code.
- Self-promotional content without developer value.

## Inclusion requirements

- Public product or documentation page; URL resolves.
- Activity signal within the last 12 months.
- Open source or a clear developer-access path.

## Entry format

```yaml
- name: Letta
  url: https://www.letta.com
  docs_url: https://docs.letta.com
  description: Open-source agent server focused on long-term memory.
  category: memory-and-state
  github: letta-ai/letta
  license: Apache-2.0
  sdks:
    - {language: Python (pip install letta-client)}
  b2_integration: ""
  last_verified: 2026-04-17
```

Field reference is identical across all awesome-* lists in this family.

## Code of conduct

This project follows standard open-source community norms. Be kind, be constructive, focus on the contribution.
