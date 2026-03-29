# Top 10 Sales Automation Skills (SkillHub.club)

> Use case: Automated sales workflow — ICP creation & filtering, pitch creation, LinkedIn automation, email outreach
> Researched: 2026-03-29

| # | Skill | Score | Security | Pipeline Stage |
|---|-------|-------|----------|----------------|
| 1 | **ICP Builder** | 9.5 | LOW | Define your ideal customer with weighted scoring |
| 2 | **Prospect** (Anthropic) | 9.2 | LOW | Natural language ICP → ranked leads with contacts |
| 3 | **B2B Sales Prospecting** | 9.0 | MEDIUM | 200M+ database, bulk list building |
| 4 | **Lead Generation** | 8.7 | MEDIUM | Social listening for high-intent buyers |
| 5 | **Intent Signal Aggregator** | 8.5 | LOW | Timing outreach by funding/hiring signals |
| 6 | **Alex Hormozi Pitch** | 8.8 | LOW | $100M Offers methodology for irresistible pitches |
| 7 | **LinkedIn Lead Gen** | 8.6 | MEDIUM | LinkedIn search + gap analysis + messaging |
| 8 | **Draft Outreach** (Anthropic) | 9.0 | LOW | Research-then-write personalized outreach |
| 9 | **Cold Email** | 8.8 | LOW-MED | 3 frameworks (OPPA/QVA/TIA), 35-day sequences |
| 10 | **Sequence Load** (Anthropic) | 8.5 | LOW | Bulk-enroll leads into Apollo sequences |

---

## Summary

**Goal:** Build an end-to-end automated sales pipeline — from defining who to sell to, through finding and qualifying leads, to pitching and outreach at scale.

**Top finding:** The 10 skills below cover the full pipeline. Three are by @anthropics (official) and seven by community authors. The @anthropics skills (Prospect, Draft Outreach, Sequence Load) form a strong core when paired with Apollo CRM. Community skills fill gaps in ICP methodology, pitch frameworks, and social listening.

**Total cost for skill installation:** Free (all skills are free to install locally).

**External dependencies cost:** Apollo ($0–$99/mo), Explorium (paid API), Xpoz (free tier), Apify ($5/mo free tier). You can start with zero cost using skills #1, #5, #6, #8 which need no external APIs.

**Security summary:** No critical issues found. Skills #3, #4, #7, #9 require external API keys — always store in env vars, never in skill files. Skill #4 (Lead Generation) requires OAuth to Xpoz which is a third-party service — verify their privacy policy. All skills are markdown instruction files, not executables.

**Pipeline flow:**
```
ICP Creation → Lead Discovery & Filtering → Pitch Creation → LinkedIn Outreach → Email Sequences → Automation
   [1]              [2,3,4,5]                   [6]               [7]              [8,9]            [10]
```

---

## Install Commands (all platforms)

Each skill below shows Claude-only install. To install across all three platforms:

```bash
# Template: install to Claude Code, Codex CLI, and OpenClaw
SKILL_NAME="skill-name-here"
for dir in ~/.claude/skills ~/.codex/skills ~/.openclaw/skills; do
  mkdir -p "$dir/$SKILL_NAME"
  cp SKILL.md "$dir/$SKILL_NAME/SKILL.md"
done
```

---

## Rankings

### 1. ICP Builder — Score: 9.5/10

- **URL:** https://www.skillhub.club/skills/openclaw-skills-icp-builder
- **Author:** @openclaw
- **Stage:** ICP Creation
- **What it does:** Guides you through building Ideal Customer Profiles using a structured, data-driven methodology with scoring models.
- **Key features:**
  - Five-step framework (Gather Inputs → Company-Level Profile → Buyer Persona → Scoring Model → Anti-ICP Definition)
  - Weighted scoring matrix: industry 25%, company size 20%, pain severity 25%, budget 15%, accessibility 15%
  - Anti-ICP definition (who NOT to sell to)
- **Use case:** Start here. Define exactly who your ideal customer is before running any prospecting. The scoring model lets you auto-rank leads later in the pipeline.
- **Security:** LOW RISK. Pure methodology skill — no external API calls, no data sent anywhere. Markdown instructions only.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/icp-builder && cp SKILL.md ~/.claude/skills/icp-builder/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/icp-builder && cp SKILL.md ~/.codex/skills/icp-builder/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/icp-builder && cp SKILL.md ~/.openclaw/skills/icp-builder/SKILL.md`

---

### 2. Prospect — Score: 9.2/10

- **URL:** https://www.skillhub.club/skills/anthropics-knowledge-work-plugins-prospect
- **Author:** @anthropics
- **Stage:** ICP Filtering / Lead Discovery
- **What it does:** Full ICP-to-leads pipeline. Describe your ideal customer in plain English, get a ranked table of enriched decision-maker leads with emails and phone numbers.
- **Key features:**
  - Natural language ICP input
  - Company search + firmographic enrichment (revenue, funding, headcount)
  - Decision-maker identification + contact enrichment
  - Lead ranking by ICP fit
- **Requires:** Apollo MCP integration
- **Use case:** After defining your ICP with skill #1, feed it into Prospect to get a ranked list of real leads with verified contact info. This is the bridge between "who do I want" and "here are their emails."
- **Security:** LOW RISK. Official @anthropics skill. Requires Apollo MCP — API key stored in MCP config, not in skill file. No suspicious patterns.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/prospect && cp SKILL.md ~/.claude/skills/prospect/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/prospect && cp SKILL.md ~/.codex/skills/prospect/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/prospect && cp SKILL.md ~/.openclaw/skills/prospect/SKILL.md`

---

### 3. B2B Sales Prospecting Agent — Score: 9.0/10

- **URL:** https://www.skillhub.club/skills/openclaw-skills-explorium-sales-prospecting
- **Author:** @openclaw
- **Stage:** Lead Prospecting
- **What it does:** Searches 200M+ companies and contacts filtered by industry, size, tech stack, location, and job title. Returns verified emails and phones.
- **Key features:**
  - ICP-based search across 200M+ records
  - Buying intent detection + growth signal filtering
  - Bulk list building (1,000+ per query)
  - CSV export for CRM import
- **Requires:** Python 3.8+, Explorium AgentSource API key
- **Use case:** When you need volume. Prospect (#2) is great for targeted lists; this one is for building large prospecting databases filtered by your ICP criteria. Export to CSV and feed into your CRM or sequence tool.
- **Security:** MEDIUM RISK. Requires Explorium API key — store in env var (`EXPLORIUM_API_KEY`), never paste into skill file. Sends queries to Explorium's external API. Verify Explorium's data handling/privacy policy.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/b2b-prospecting && cp SKILL.md ~/.claude/skills/b2b-prospecting/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/b2b-prospecting && cp SKILL.md ~/.codex/skills/b2b-prospecting/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/b2b-prospecting && cp SKILL.md ~/.openclaw/skills/b2b-prospecting/SKILL.md`

---

### 4. Lead Generation (Social Listening) — Score: 8.7/10

- **URL:** https://www.skillhub.club/skills/openclaw-skills-lead-generation
- **Author:** @openclaw
- **Stage:** Intent-Based Lead Discovery
- **What it does:** Finds high-intent buyers from live social conversations on Twitter, Instagram, and Reddit. Auto-researches your product first.
- **Key features:**
  - 1.5B+ indexed social posts via Xpoz
  - Intelligent lead scoring (1-10 scale)
  - Three-tier classification: Hot / Warm / Watchlist
  - Pre-drafted outreach templates
- **Requires:** mcporter (Node.js), Xpoz MCP OAuth (free account)
- **Use case:** Catches people actively complaining about problems your product solves. "I hate my current CRM" → that's a hot lead. Complements database prospecting (#3) with real-time intent signals.
- **Security:** MEDIUM RISK. Requires OAuth to Xpoz (third-party social indexing service). Review Xpoz privacy policy before granting OAuth. mcporter is an npm package — verify it's legitimate (`npm info mcporter`). Social data scraping may have legal implications depending on jurisdiction.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/lead-generation && cp SKILL.md ~/.claude/skills/lead-generation/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/lead-generation && cp SKILL.md ~/.codex/skills/lead-generation/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/lead-generation && cp SKILL.md ~/.openclaw/skills/lead-generation/SKILL.md`

---

### 5. Intent Signal Aggregator — Score: 8.5/10

- **URL:** https://www.skillhub.club/skills/gked2121-claude-skills-intent-signal-aggregator
- **Author:** @gked2121
- **Stage:** Lead Prioritization
- **What it does:** Monitors buyer intent signals across the web — job postings, tech changes, funding rounds, leadership changes — to identify the best time to reach out.
- **Key features:**
  - Three-tier signal classification (high / medium / low intent)
  - Hot account identification
  - Outreach timing recommendations
  - Win-rate analytics by signal type
- **Use case:** Timing is everything. A company that just raised funding or posted a relevant job opening is 3-5x more likely to buy. Layer this on top of your lead lists from #2/#3 to prioritize who to contact first.
- **Security:** LOW RISK. Methodology-focused skill. May instruct agent to web-search for signals — standard browser-level access, no API keys required.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/intent-signals && cp SKILL.md ~/.claude/skills/intent-signals/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/intent-signals && cp SKILL.md ~/.codex/skills/intent-signals/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/intent-signals && cp SKILL.md ~/.openclaw/skills/intent-signals/SKILL.md`

---

### 6. Alex Hormozi Pitch — Score: 8.8/10

- **URL:** https://www.skillhub.club/skills/buttercupck-bcck-vault-alex-hormozi-pitch
- **Author:** @buttercupck
- **Stage:** Pitch Creation
- **What it does:** Create irresistible offers and pitches using Alex Hormozi's methodology from $100M Offers.
- **Key features:**
  - Value Equation framework (Dream Outcome × Perceived Likelihood) / (Time × Effort)
  - Four guarantee types (unconditional, conditional, outcome-based, anti-guarantee)
  - MAGIC naming formula
  - Value stack and bonus construction
  - Scarcity/urgency strategies
- **Use case:** Before you write a single email or LinkedIn message, craft your offer. This skill turns "we sell X" into "here's why saying no is irrational." Use the output to fuel your outreach messaging in skills #7-#9.
- **Security:** LOW RISK. Pure methodology skill — no external calls, no API keys, no data exfiltration vectors. Markdown instructions only.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/hormozi-pitch && cp SKILL.md ~/.claude/skills/hormozi-pitch/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/hormozi-pitch && cp SKILL.md ~/.codex/skills/hormozi-pitch/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/hormozi-pitch && cp SKILL.md ~/.openclaw/skills/hormozi-pitch/SKILL.md`

---

### 7. LinkedIn Lead Gen — Score: 8.6/10

- **URL:** https://www.skillhub.club/skills/openclaw-skills-linkedin-lead-generation
- **Author:** @openclaw
- **Stage:** LinkedIn Automation
- **What it does:** Searches and verifies founders on LinkedIn, identifies high-value prospects, and generates outreach messages.
- **Key features:**
  - Industry-targeted LinkedIn search
  - 2nd-degree connection filtering
  - Website gap analysis (speed, mobile, SEO, e-commerce)
  - Professional HTML/PDF reports
  - Problem-first messaging templates
- **Use case:** LinkedIn is where B2B decision-makers live. This skill finds them, analyzes their company's weak points (e.g. slow website, no mobile optimization), and generates messages that lead with their specific problems — not your pitch.
- **Security:** MEDIUM RISK. LinkedIn scraping may violate LinkedIn ToS — use at your own discretion. Website gap analysis involves fetching external URLs. No API keys required but generates reports that could contain scraped PII — store securely.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/linkedin-lead-gen && cp SKILL.md ~/.claude/skills/linkedin-lead-gen/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/linkedin-lead-gen && cp SKILL.md ~/.codex/skills/linkedin-lead-gen/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/linkedin-lead-gen && cp SKILL.md ~/.openclaw/skills/linkedin-lead-gen/SKILL.md`

---

### 8. Draft Outreach — Score: 9.0/10

- **URL:** https://www.skillhub.club/skills/anthropics-knowledge-work-plugins-draft-outreach
- **Author:** @anthropics
- **Stage:** Email + LinkedIn Outreach
- **What it does:** Researches a prospect then drafts personalized outreach. Three-step workflow: Research → Draft → Deliver.
- **Key features:**
  - Auto-researches prospect before writing
  - Personalized openers from prospect's real activity
  - Multiple output formats (email, LinkedIn DM)
  - Follow-up sequences with timing (Days 3, 7, 14)
  - Subject line alternatives
- **Use case:** The personalization engine. Feed it a lead from your prospecting pipeline, and it researches them (recent posts, company news, role changes) then writes outreach that doesn't sound like a template. Works for both email and LinkedIn.
- **Security:** LOW RISK. Official @anthropics skill. Web research uses standard browsing. Enhanced mode uses CRM data already in your system. No external data exfiltration.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/draft-outreach && cp SKILL.md ~/.claude/skills/draft-outreach/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/draft-outreach && cp SKILL.md ~/.codex/skills/draft-outreach/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/draft-outreach && cp SKILL.md ~/.openclaw/skills/draft-outreach/SKILL.md`

---

### 9. Cold Email — Score: 8.8/10

- **URL:** https://www.skillhub.club/skills/openclaw-skills-cs-cold-email
- **Author:** @openclaw
- **Stage:** Email Sequences
- **What it does:** Write, improve, and sequence B2B cold outreach emails. Three modes: first email creation, sequence building, performance iteration.
- **Key features:**
  - Three writing frameworks: OPPA (Observation-Problem-Proposition-Ask), QVA (Question-Value-Ask), TIA (Trigger-Insight-Ask)
  - Peer-level tone enforcement (no begging, no "just checking in")
  - 35-day cadence template (Days 1, 3, 7, 14, 21, 35)
  - Deliverability guidance (SPF, DKIM, DMARC)
  - Performance diagnosis for underperforming sequences
- **Requires:** Dedicated sending domain, email authentication, domain warmup (4-6 weeks)
- **Use case:** Draft Outreach (#8) writes individual emails; this skill builds the full sequence strategy. Use OPPA for first touch, QVA for follow-ups, and TIA for re-engagement. The performance iteration mode is gold — feed it your open/reply rates and it rewrites underperforming steps.
- **Security:** LOW-MEDIUM RISK. Includes a Python analysis script — review before running. Deliverability setup (SPF, DKIM, DMARC) modifies DNS records — understand what you're changing. No external API calls from the skill itself.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/cold-email && cp SKILL.md ~/.claude/skills/cold-email/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/cold-email && cp SKILL.md ~/.codex/skills/cold-email/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/cold-email && cp SKILL.md ~/.openclaw/skills/cold-email/SKILL.md`

---

### 10. Sequence Load — Score: 8.5/10

- **URL:** https://www.skillhub.club/skills/anthropics-knowledge-work-plugins-sequence-load
- **Author:** @anthropics
- **Stage:** Outreach Automation
- **What it does:** Find leads matching criteria and bulk-add them to an Apollo outreach sequence. Handles enrichment, contact creation, deduplication, and enrollment.
- **Key features:**
  - Lead discovery by job title, seniority, industry, company size, location
  - Contact enrichment + deduplication
  - Bulk sequence enrollment
  - Email account management
- **Requires:** Apollo CRM API access via MCP
- **Use case:** The last mile. Once you've built your ICP (#1), found leads (#2-#5), crafted your pitch (#6), and written your sequences (#8-#9), this skill loads everything into Apollo and hits go. Handles dedup so you don't email the same person twice.
- **Security:** LOW RISK. Official @anthropics skill. Requires Apollo API via MCP — key stored in MCP config. Consumes Apollo credits when enriching contacts — skill explicitly asks for approval before credit-consuming operations.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/sequence-load && cp SKILL.md ~/.claude/skills/sequence-load/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/sequence-load && cp SKILL.md ~/.codex/skills/sequence-load/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/sequence-load && cp SKILL.md ~/.openclaw/skills/sequence-load/SKILL.md`

---

## Security Overview

| # | Skill | Risk Level | Key Concern |
|---|-------|-----------|-------------|
| 1 | ICP Builder | LOW | None — pure methodology |
| 2 | Prospect | LOW | Official @anthropics, Apollo MCP |
| 3 | B2B Sales Prospecting | MEDIUM | Explorium API key — use env vars |
| 4 | Lead Generation | MEDIUM | Xpoz OAuth, mcporter npm package — verify both |
| 5 | Intent Signal Aggregator | LOW | Web search only, no API keys |
| 6 | Alex Hormozi Pitch | LOW | None — pure methodology |
| 7 | LinkedIn Lead Gen | MEDIUM | LinkedIn ToS, PII in reports |
| 8 | Draft Outreach | LOW | Official @anthropics |
| 9 | Cold Email | LOW-MEDIUM | Includes Python script — review before running |
| 10 | Sequence Load | LOW | Official @anthropics, asks before using credits |

**General rule:** Always `grep -iE "(curl|wget|fetch|\.ssh|\.env|credentials|eval|exec|base64)" SKILL.md` before installing any skill.

---

## Honorable Mentions

| Skill | URL | Why it's worth noting |
|-------|-----|----------------------|
| **Founder Sales** | [link](https://www.skillhub.club/skills/liqiongyu-lenny-skills-plus-founder-sales) | Full founder sales sprint pack — great if you're a founder doing sales yourself |
| **Lead Hunter** | [link](https://www.skillhub.club/skills/openclaw-skills-lead-hunter) | Multi-platform lead discovery (X, GitHub, Product Hunt) |
| **Lead Research Assistant** | [link](https://www.skillhub.club/skills/microck-ordinary-claude-skills-lead-research-assistant) | No API required — good starting point if you don't have Apollo/Explorium yet |
| **positioning-icp** | [link](https://www.skillhub.club/skills/tech-leads-club-agent-skills-positioning-icp) | Adds positioning + messaging architecture on top of ICP |
| **Email Marketing Command Center** | [link](https://www.skillhub.club/skills/openclaw-skills-afrexai-email-marketing) | Full email marketing system if you expand beyond cold outreach |
| **Ultimate Lead Scraper** | [link](https://www.skillhub.club/skills/openclaw-skills-ultimate-lead-scraper-ai-outreach) | Multi-source scraping (Yellow Pages, Google Maps, LinkedIn, Yelp) |

---

## Quick Start: Recommended Install Order

1. Install **ICP Builder** → define your ideal customer
2. Install **Alex Hormozi Pitch** → craft your offer
3. Install **Prospect** + **B2B Sales Prospecting Agent** → find leads
4. Install **Intent Signal Aggregator** → prioritize who to contact first
5. Install **LinkedIn Lead Gen** → LinkedIn outreach channel
6. Install **Draft Outreach** + **Cold Email** → email outreach channel
7. Install **Sequence Load** → automate at scale
