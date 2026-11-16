---
title: "Claude Is Brilliant — But His Memory Is a Liability"
date: "2026-05-10"
medium: "https://klangmeister.medium.com/claude-is-brilliant-but-his-memory-is-a-liability-7b28a02bd77c"
author: "hans-mueller"
lead: "Claude is extraordinary.He writes architecture, explains systems, untangles codebases, and often understands your own project better than you do."
tags: ["vault", "memories", "claude", "pypi", "mcp-server"]
---

# Claude Is Brilliant — But His Memory Is a Liability

*Originally published on [Medium](https://klangmeister.medium.com/claude-is-brilliant-but-his-memory-is-a-liability-7b28a02bd77c) · 2026-05-10*

[Home](../README.md) · [Buzzer of the Day](../daily/README.md) · [Weekly](../weekly/README.md) · [Monthly](../monthly/README.md) · [Yearly](../yearly/README.md) · [Glossary](../glossary/README.md) · [Features](README.md)

> Claude is extraordinary.  
> He writes architecture, explains systems, untangles codebases, and often understands your own project better than you do.

And yet, every time you open the CLI, there’s that familiar moment:

A pause.  
A breath.  
A tiny prayer:

**“Please don’t crash. Not now.”**

Because if it crashes, everything evaporates — the insights, the decisions, the half‑formed ideas, the subtle reasoning that only existed in that one fragile session.

Claude is a genius.  
But a genius with amnesia.

### The Paradox of Working With Claude

Claude can analyze a 3,600‑file monorepo.  
He can outline a refactoring strategy that would take a human a week.  
He can reason across architecture, product, and code in one sweep.

But ask him tomorrow what you decided today, and he’ll look at you like you’ve never met.

This isn’t a flaw in intelligence.  
It’s a flaw in memory.

And that’s where the **Claude Vault** comes in.

### The Vault: A Second Brain for an AI That Doesn’t Have One

The Vault is a persistent, structured memory layer that survives crashes, sessions, and context resets.

It’s built from three components:

### 1. Obsidian Vault — Declarative Memory

A clean, navigable knowledge base:

    logs/
    permanent/
    fleeting/
    inbox/
    references/

This is where Claude’s long‑term thinking actually lives.

### 2. Graphify — Structural Memory

Graphify turns your entire repository into a navigable code graph.

Official repo:  
<https://github.com/safishamsi/graphify>

Nodes = files and functions  
Edges = imports, calls, dependencies  
Output lives under:

    graphify/<project>/graphify-out/graph.json

Instead of “read the whole repo,” you ask:

**“Which controllers call LinkApiCli?”**

And Graphify answers instantly.

### 3. Junctions — Zero‑Drift Repo Mirror

A live, read‑only mirror of the real repo inside the Vault.

No copy‑paste.  
No divergence.  
No outdated documentation.

Junction example:

    repo-link/arc42  →  <your real repo>/arc42

This keeps your Vault and your repo in perfect sync.

### Why This Matters

Without the Vault:  
Claude is brilliant but volatile.

With the Vault:  
Claude becomes predictable, stable, and context‑aware.

- /resume loads the last three logs + decisions
- /save writes a clean session summary
- Permanent notes capture concepts, not noise
- Junctions eliminate drift
- Graphify replaces blind searching with structured queries

This isn’t “nice to have.”  
It solves real problems.

### Bonus: Cavemen as MCP Server

And then there’s **Cavemen MCP** — the unexpected hero.

Cavemen is a minimal, robust MCP server implementation that avoids the typical pitfalls described in Claude Code’s troubleshooting guides:

Claude Code troubleshooting (official):  
<https://code.claude.com/docs/llms.txt>

Common MCP issues documented here:  
https://deepwiki.com/steipete/claude-code-mcp

Cavemen avoids:

- PATH issues
- missing CLI binaries
- permission prompts
- “CLI not found” loops
- unexpected token errors
- random crashes

It looks primitive, but it’s rock‑solid.

In a world where LLMs hallucinate, drift, and forget, Cavemen is the anchor.

### Related Tools & Integrations

### Claude Vault MCP (PyPI)

https://pypi.org/project/claude-vault-mcp/

A lightweight integration layer that connects Claude Code with your Vault.

### Graphify (GitHub)

<https://github.com/safishamsi/graphify>

### Claude Code Troubleshooting

<https://code.claude.com/docs/llms.txt>

### MCP Server Troubleshooting (Deepwiki)

https://deepwiki.com/steipete/claude-code-mcp

### The Minimal dr.claude.md

If Claude gets a memory, he also needs rules.  
Not 40 pages of philosophy.  
Just the essentials.

A minimized version:

    # CLAUDE

    Use the Vault as memory.
    Read before you guess.
    Link before you repeat.
    Persist sessions, not emotions.
    Work with Graphify.
    Respect decisions.md.
    Stay consistent.

That’s it.  
Everything else is noise.
