# Agency Agents

> 100+ specialized AI agent personalities — [github.com/msitarzewski/agency-agents](https://github.com/msitarzewski/agency-agents)

## What is it?

A collection of 100+ specialized AI agent personalities across divisions: Engineering (30+), Design, Sales, Marketing (40+ including regional specialists), Product, Project Management, Testing, Support, Spatial Computing, and more.

Each agent has distinct expertise, communication style, and battle-tested workflows — not generic templates.

**License**: MIT

## How to Install

### Option 1 — Claude Code (recommended)

```bash
git clone https://github.com/msitarzewski/agency-agents.git
cp -r agency-agents/* ~/.claude/agents/
```

### Option 2 — Multi-tool install script

```bash
git clone https://github.com/msitarzewski/agency-agents.git
cd agency-agents
./scripts/install.sh                  # install for all supported tools
./scripts/install.sh --tool cursor    # or target a specific tool
./scripts/install.sh --tool copilot
./scripts/install.sh --tool aider
./scripts/install.sh --tool windsurf
./scripts/install.sh --tool kimi
```

### Option 3 — Reference only

Browse the repo and adapt individual agent files as needed.

## Usage

Once installed, reference agents by their role in Claude Code sessions. They act as specialized personas with domain expertise.
