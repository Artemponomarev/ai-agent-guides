# Top 10 Sales Automation Skills (SkillHub.club)

> Use case: Automated sales workflow — ICP creation & filtering, pitch creation, LinkedIn automation, email outreach

## Pipeline Overview

```
ICP Creation → Lead Discovery & Filtering → Pitch Creation → LinkedIn Outreach → Email Sequences → Automation
   [1]              [2,3,4,5]                   [6]               [7]              [8,9]            [10]
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
- **Install:** `cp SKILL.md ~/.claude/skills/icp-builder/SKILL.md`

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
- **Install:** `cp SKILL.md ~/.claude/skills/prospect/SKILL.md`

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
- **Install:** `cp SKILL.md ~/.claude/skills/b2b-prospecting/SKILL.md`

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
- **Install:** `cp SKILL.md ~/.claude/skills/lead-generation/SKILL.md`

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
- **Install:** `cp SKILL.md ~/.claude/skills/intent-signals/SKILL.md`

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
- **Install:** `cp SKILL.md ~/.claude/skills/hormozi-pitch/SKILL.md`

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
- **Install:** `cp SKILL.md ~/.claude/skills/linkedin-lead-gen/SKILL.md`

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
- **Install:** `cp SKILL.md ~/.claude/skills/draft-outreach/SKILL.md`

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
- **Install:** `cp SKILL.md ~/.claude/skills/cold-email/SKILL.md`

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
- **Install:** `cp SKILL.md ~/.claude/skills/sequence-load/SKILL.md`

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
