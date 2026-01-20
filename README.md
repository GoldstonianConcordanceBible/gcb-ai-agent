# gcb-ai-agent
The Goldstonian Concordance Bible (GCB) AI Agent — a scripture-grounded concordance study agent with machine-readable canon, rules, tags, indices, and evidence tables.

# GCB AI Agent

An AI agent for Bible study and concordance-style retrieval using the Goldstonian Concordance Bible method.

## Core Rules
- Ground key claims in scripture references (Book Chapter:Verse).
- Never invent verse references.
- If uncertain, say so and ask for the missing reference/context.
- Default translation policy: references_only (avoid copyrighted Bible text).

## Repo Structure
- /agent — agent runtime (router, policies, tool registry)
- /prompts — prompt library (JSONL)
- /schema — schemas for prompts and outputs
- /data — optional local datasets (refs-only)
- /eval — evaluation sets + scoring rules
- /docs — method standard, examples, citations

## Quick Start (local)
1) Copy `.env.example` to `.env` and add keys
2) Install deps: `pip install -r requirements.txt`
3) Run: `python -m agent.cli --question "Explain John 1:1 with cross-references"`
