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
3. Save it to your agent's skills directory:
   - **Claude Code**: `~/.claude/skills/<skill-name>/SKILL.md`
   - **Codex CLI**: `~/.codex/skills/<skill-name>/SKILL.md`
   - **OpenClaw**: `~/.openclaw/skills/<skill-name>/SKILL.md`

### Option 2 — CLI

```bash
npx @skill-hub/cli install [skill-name]
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
