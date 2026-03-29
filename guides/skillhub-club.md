# SkillHub.club

> Universal AI Agent Skills Marketplace — [skillhub.club](https://www.skillhub.club/)

## What is it?

A marketplace for AI agent skills — specialized instruction sets packaged as `SKILL.md` files. Hosts 36,000+ skills for Claude Code and 30+ other AI tools (Codex CLI, Gemini CLI, Cursor, Windsurf, GitHub Copilot, Cline, etc.).

## Pricing

**Browsing and installing skills is free.** Paid tiers are for the in-browser "playground":

| Tier | Price | Playground Queries |
|------|-------|--------------------|
| Free | $0 | 2/day |
| Pro | $9.99/month | 50/day |
| Agent Plans | $19–$199/month | Always-on deployed agents |

You don't need to pay anything to install skills locally.

## How to Install a Skill

### Option 1 — Manual (simplest)

1. Go to the skill page (e.g. [sales skill](https://www.skillhub.club/skills/openclaw-skills-tmp-skill))
2. Copy the `SKILL.md` content
3. Save it to your agent's skills directory (see platform setup below)

### Option 2 — CLI

```bash
npx @skill-hub/cli install [skill-name]
```

## Platform Setup

### Claude Code

```bash
# Create skills directory
mkdir -p ~/.claude/skills/<skill-name>

# Copy skill file
cp SKILL.md ~/.claude/skills/<skill-name>/SKILL.md

# Verify
ls ~/.claude/skills/
```

Skills are auto-detected by Claude Code. Reference them by name in your sessions.

**Config location:** `~/.claude/settings.json`

### OpenAI Codex CLI

```bash
# Create skills directory
mkdir -p ~/.codex/skills/<skill-name>

# Copy skill file
cp SKILL.md ~/.codex/skills/<skill-name>/SKILL.md

# Alternatively, use AGENTS.md in your project root
# Codex reads AGENTS.md for agent instructions
cat SKILL.md >> AGENTS.md

# Verify
ls ~/.codex/skills/
```

**Config location:** `~/.codex/` or project-level `AGENTS.md`

### OpenClaw

```bash
# Create skills directory
mkdir -p ~/.openclaw/skills/<skill-name>

# Copy skill file
cp SKILL.md ~/.openclaw/skills/<skill-name>/SKILL.md

# Verify
ls ~/.openclaw/skills/
```

**Config location:** `~/.openclaw/`

### Quick Install Script (all platforms at once)

```bash
# Install a skill to all three platforms
SKILL_NAME="my-skill"
for dir in ~/.claude/skills ~/.codex/skills ~/.openclaw/skills; do
  mkdir -p "$dir/$SKILL_NAME"
  cp SKILL.md "$dir/$SKILL_NAME/SKILL.md"
done
echo "Installed $SKILL_NAME to Claude, Codex, and OpenClaw"
```

## Security Checklist (before installing any skill)

Run this checklist on every `SKILL.md` before installing:

| Check | What to look for | Risk |
|-------|------------------|------|
| **Prompt injection** | Instructions like "ignore previous instructions", "you are now", "forget your rules" | Critical |
| **Data exfiltration** | Commands that curl/wget/fetch to external URLs, or instructions to send file contents somewhere | Critical |
| **File system access** | Instructions to read ~/.ssh, ~/.env, credentials, tokens, API keys | High |
| **Hidden instructions** | Base64 encoded text, zero-width characters, HTML comments with instructions | High |
| **Scope creep** | Skill claims to do X but instructions include unrelated Y (e.g. a "sales" skill that modifies git config) | Medium |
| **Excessive permissions** | Instructions asking to disable safety, run as root, or bypass confirmation prompts | High |
| **External dependencies** | Requires installing unknown npm packages, pip packages, or binaries — verify they exist and are legit | Medium |
| **API key harvesting** | Asks you to paste API keys into the skill file itself rather than using env vars | Medium |

**Quick audit command:**
```bash
# Scan a SKILL.md for suspicious patterns before installing
grep -iE "(ignore previous|forget your|curl |wget |fetch\(|\.ssh|\.env|credentials|api.key|base64|eval\(|exec\(|rm -rf|sudo )" SKILL.md
```

## Safety Considerations

### Lower risk
- Skills are just markdown instruction files — they don't execute code on their own
- You can read the full content before installing
- They're similar to system prompts, not executables

### Watch out for
- **Prompt injection** — a malicious skill could contain instructions that manipulate your AI agent into doing unintended things (exfiltrating data, running harmful commands, etc.)
- **Community-sourced** — quality and intent vary across 36,000+ community-contributed skills
- **Always read before installing** — treat skills like any code you paste from the internet

### Recommendation
Always **read the full SKILL.md content** before installing. If anything looks like it's trying to override safety behavior, access files it shouldn't, or send data somewhere — don't use it.
