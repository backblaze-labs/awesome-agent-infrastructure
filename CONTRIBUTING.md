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

Every entry is a recommendation to developers, so each one must pass all four checks:

1. **In scope** for this list (see above).
2. **Usable today:**
   - the URL resolves;
   - a dated sign of activity in the last 12 months (release, commit, or dated changelog);
   - a developer access path: a documented public API or SDK with self-serve signup (paid is fine; waitlists and "contact sales" are not), public source with an install path, or downloadable datasets/weights with a stated license.
3. **Not already listed.** One entry per product: a vendor's per-model SDKs, or an API plus its MCP server, are one entry. New versions update the existing entry.
4. **Fits an existing category** in `categories.yaml`.

Self-submissions are welcome and held to the same bar. Low star counts are fine; clear docs matter more.

**We don't accept:** thin resellers of a single model, unofficial access to products that have no official API, consumer apps with no API/CLI/library, guides or directories of other tools (unless this list accepts them above), products whose primary purpose is adult content, and tools built to evade access controls (e.g. CAPTCHA solving) or impersonate real people.

**Writing the entry:**
- One factual sentence on what it does, ≤300 characters. No marketing adjectives, superlatives ("fastest", "#1"), or pricing/free-tier claims.
- Canonical URLs only: no `utm_`, referral, or affiliate parameters.
- `license` is the SPDX id from the repo; `sdks.language` is just the language name.
- Leave `b2_integration` as `""`; maintainers set it.
- Add or edit only your own product's entry.

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

## What happens after you submit

A maintainer checks the entry against the requirements above. Small fixes (formatting, URLs, description length, merge conflicts) are made for you, keeping you as the commit author. If we need information only you have, we'll ask one specific question; if the entry is out of scope, we'll close the PR with the reason.

## Code of conduct

This project follows standard open-source community norms. Be kind, be constructive, focus on the contribution.
