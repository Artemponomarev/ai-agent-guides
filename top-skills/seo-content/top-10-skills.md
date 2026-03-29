# Top 10 SEO & Content Writing Skills (SkillHub.club)

> Use case: Autorun blog on site + LinkedIn posting — SEO research, content creation, blog publishing, social distribution
> Researched: 2026-03-29

| # | Skill | Score | Security | Pipeline Stage |
|---|-------|-------|----------|----------------|
| 1 | **Content Engine** | 9.5 | LOW | All-in-one: SEO research → writing → blog → social |
| 2 | **SEO Audit** | 9.2 | LOW | Technical + on-page SEO diagnostics |
| 3 | **SEO Research Master** | 9.0 | LOW | Keyword research + competitor analysis |
| 4 | **Programmatic SEO** | 8.8 | LOW | Scalable SEO page generation at volume |
| 5 | **Voice-Matched Content** | 8.7 | LOW | Authentic brand voice (not AI-sounding) |
| 6 | **Social Media Post** | 9.0 | LOW | LinkedIn + X + Threads with algorithm-aware formatting |
| 7 | **WordPress Publisher** | 8.5 | MEDIUM | Direct blog publishing via WordPress API |
| 8 | **Social Media Scheduler** | 8.6 | LOW | Weekly batch content for LinkedIn/X/Instagram |
| 9 | **AI Pattern Detection** | 8.4 | LOW | Remove AI-sounding patterns from content |
| 10 | **Rank Tracker** | 8.3 | LOW | Track keyword rankings + SERP changes over time |

---

## Summary

**Goal:** Fully automated content pipeline — research keywords, write SEO-optimized blog posts, publish to site, distribute on LinkedIn and social media.

**Top finding:** **Content Engine** (@openclaw) is the single most comprehensive skill — it covers the entire pipeline from SEO research through content writing, blog formatting (WordPress/Ghost/Notion/Hugo/Jekyll), and social promotion posts for LinkedIn/Twitter/Reddit. Pair it with SEO Audit (#2) for diagnostics and Voice-Matched Content (#5) to avoid sounding like AI.

**Total cost for skill installation:** Free (all skills are free to install locally).

**External dependencies cost:** WordPress API (free with self-hosted), no other paid APIs required for the core pipeline. Rank Tracker may need SERP API access for automated monitoring.

**Security summary:** Very low risk overall. Most skills are pure methodology/instruction sets with no external API calls. WordPress Publisher (#7) is the only one requiring API credentials — store in env vars. No prompt injection or data exfiltration concerns detected.

**Pipeline flow:**
```
SEO Research → Content Writing → Quality Check → Blog Publishing → Social Distribution → Rank Monitoring
   [2,3,4]        [1,5]            [9]              [7]              [6,8]               [10]
```

---

## Install Commands (all platforms)

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

### 1. Content Engine — Score: 9.5/10

- **URL:** https://www.skillhub.club/skills/openclaw-skills-content-engine
- **Author:** @openclaw | Tries: 3.5k | Rating: B-A
- **Stage:** End-to-end content pipeline
- **What it does:** Full-stack content creation from research to publication. Analyzes competitor articles, identifies content gaps, generates SEO-optimized blog posts with brand voice.
- **Key features:**
  - Competitor article analysis + content gap identification
  - SEO-optimized blog post generation with brand voice
  - Meta descriptions + internal link suggestions
  - Multi-platform formatting: WordPress, Ghost, Notion, Hugo, Jekyll
  - Social media promotion posts for LinkedIn, Twitter/X, Reddit
- **Use case:** Your primary workhorse. Point it at a topic, it researches competitors, finds gaps, writes an SEO-optimized post, formats it for your blog platform, and generates LinkedIn/Twitter promotion posts. Covers 80% of the pipeline alone.
- **Security:** LOW RISK. Methodology skill with web research. No API keys required. No external data sent.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/content-engine && cp SKILL.md ~/.claude/skills/content-engine/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/content-engine && cp SKILL.md ~/.codex/skills/content-engine/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/content-engine && cp SKILL.md ~/.openclaw/skills/content-engine/SKILL.md`

---

### 2. SEO Audit — Score: 9.2/10

- **URL:** https://www.skillhub.club/skills/coreyhaines31-marketingskills-seo-audit
- **Author:** @coreyhaines31 | Tries: 17.1k | Rating: B-A
- **Stage:** SEO diagnostics
- **What it does:** Audit, review, and diagnose SEO issues on a site. Covers technical SEO, on-page SEO, meta tags review, and SEO health checks.
- **Key features:**
  - Technical SEO audit (crawlability, indexing, site speed)
  - On-page SEO review (titles, meta descriptions, headings, content)
  - Meta tags and structured data validation
  - Actionable fix recommendations with priority ranking
- **Use case:** Run this before you start writing. Audit your blog's current SEO health, find technical issues holding you back, and get a prioritized fix list. Re-run monthly to catch regressions.
- **Security:** LOW RISK. Analyzes your own site — no external API keys, no data exfiltration. Pure diagnostic skill.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/seo-audit && cp SKILL.md ~/.claude/skills/seo-audit/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/seo-audit && cp SKILL.md ~/.codex/skills/seo-audit/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/seo-audit && cp SKILL.md ~/.openclaw/skills/seo-audit/SKILL.md`

---

### 3. SEO Research Master — Score: 9.0/10

- **URL:** https://www.skillhub.club/skills/openclaw-skills-seo-research-master
- **Author:** @openclaw | Tries: 3.6k | Rating: B-B
- **Stage:** Keyword research + competitor analysis
- **What it does:** AI-powered SEO keyword research, competitor analysis, and content opportunity identification for any niche.
- **Key features:**
  - Keyword research with search volume and difficulty estimates
  - Competitor content analysis
  - Content opportunity/gap identification
  - Data-driven content strategy recommendations
- **Use case:** Feed it your niche and it finds the keywords worth targeting, what competitors are ranking for, and where the content gaps are. Use the output to build your editorial calendar and feed topics into Content Engine (#1).
- **Security:** LOW RISK. Web research only. No API keys required. No external data sent.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/seo-research-master && cp SKILL.md ~/.claude/skills/seo-research-master/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/seo-research-master && cp SKILL.md ~/.codex/skills/seo-research-master/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/seo-research-master && cp SKILL.md ~/.openclaw/skills/seo-research-master/SKILL.md`

---

### 4. Programmatic SEO — Score: 8.8/10

- **URL:** https://www.skillhub.club/skills/alirezarezvani-claude-skills-programmatic-seo
- **Author:** @alirezarezvani | Tries: 7.7k | Rating: B-A
- **Stage:** Scalable SEO page generation
- **What it does:** Create SEO-driven pages at scale using templates and data — location pages, comparison pages, integration pages, feature pages.
- **Key features:**
  - Template-based page generation at scale
  - Location-specific landing pages
  - Comparison and "vs" pages
  - Integration/feature pages from structured data
- **Use case:** When you need volume. Instead of writing one blog post at a time, generate 50+ SEO-optimized pages from a template + data source. Great for "best X in [city]" or "[product] vs [competitor]" pages that capture long-tail traffic.
- **Security:** LOW RISK. Template-based generation. No external APIs. No data exfiltration.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/programmatic-seo && cp SKILL.md ~/.claude/skills/programmatic-seo/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/programmatic-seo && cp SKILL.md ~/.codex/skills/programmatic-seo/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/programmatic-seo && cp SKILL.md ~/.openclaw/skills/programmatic-seo/SKILL.md`

---

### 5. Voice-Matched Content — Score: 8.7/10

- **URL:** https://www.skillhub.club/skills/openclaw-skills-voice-matched-content-system
- **Author:** @openclaw | Tries: 3.5k | Rating: B-A
- **Stage:** Brand voice / content authenticity
- **What it does:** Extract your authentic writing voice and generate content that matches it — not AI-sounding generic content.
- **Key features:**
  - Voice DNA profiling from your existing content
  - Confidence calibration (matches your certainty patterns)
  - Energy mapping (matches your pacing and intensity)
  - Platform-specific tuning (blog vs LinkedIn vs email)
- **Use case:** Critical for automation. Without this, your auto-generated blog posts and LinkedIn content will sound like ChatGPT. Feed it 5-10 of your best posts, it extracts your voice profile, then all generated content matches your style. Pair with AI Pattern Detection (#9) for double protection.
- **Security:** LOW RISK. Analyzes your own content locally. No external data sent. No API keys.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/voice-matched-content && cp SKILL.md ~/.claude/skills/voice-matched-content/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/voice-matched-content && cp SKILL.md ~/.codex/skills/voice-matched-content/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/voice-matched-content && cp SKILL.md ~/.openclaw/skills/voice-matched-content/SKILL.md`

---

### 6. Social Media Post — Score: 9.0/10

- **URL:** https://www.skillhub.club/skills/alekspetrov-navigator-social-media-post
- **Author:** @alekspetrov | Tries: 160 | Rating: A 8.3
- **Stage:** LinkedIn + social media posting
- **What it does:** Generates platform-specific posts for LinkedIn, Threads, and X with algorithm-aware formatting and engagement tactics.
- **Key features:**
  - Algorithm-aware formatting per platform
  - Character limits and platform constraints enforced
  - Engagement tactics (hooks, CTAs, hashtag strategies)
  - Multiple post variants with optimal posting time metadata
  - 2025 best practices baked in
- **Use case:** Your LinkedIn posting engine. Feed it a blog post or topic, it generates LinkedIn-optimized posts with hooks that beat the algorithm, proper formatting (line breaks, emoji usage), and posting time recommendations. Also covers X and Threads.
- **Security:** LOW RISK. Pure content generation. No API calls. No external services. No data sent anywhere.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/social-media-post && cp SKILL.md ~/.claude/skills/social-media-post/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/social-media-post && cp SKILL.md ~/.codex/skills/social-media-post/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/social-media-post && cp SKILL.md ~/.openclaw/skills/social-media-post/SKILL.md`

---

### 7. WordPress Publisher — Score: 8.5/10

- **URL:** https://www.skillhub.club/skills/aviz85-claude-skills-library-wordpress-publisher
- **Author:** @aviz85 | Rating: B-S
- **Stage:** Blog publishing automation
- **What it does:** Publish posts to WordPress directly from your agent — create, update, schedule posts via the WordPress REST API.
- **Key features:**
  - Direct WordPress post creation and publishing
  - Post scheduling for future dates
  - Category and tag management
  - Draft/publish/schedule status control
- **Requires:** WordPress site with REST API enabled, application password or API key
- **Use case:** The publishing step. Content Engine (#1) writes the post, this skill pushes it live to your WordPress blog. Set up a workflow: research → write → review → publish → promote on LinkedIn.
- **Security:** MEDIUM RISK. Requires WordPress API credentials — **store as env var** (`WP_API_KEY`), never paste into skill file. Sends content to your WordPress instance. Verify the skill doesn't send data elsewhere. API credentials grant write access to your blog — use a dedicated application password with limited scope.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/wordpress-publisher && cp SKILL.md ~/.claude/skills/wordpress-publisher/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/wordpress-publisher && cp SKILL.md ~/.codex/skills/wordpress-publisher/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/wordpress-publisher && cp SKILL.md ~/.openclaw/skills/wordpress-publisher/SKILL.md`

---

### 8. Social Media Scheduler — Score: 8.6/10

- **URL:** https://www.skillhub.club/skills/openclaw-skills-weekly-content-planner
- **Author:** @openclaw | Tries: 3.5k | Rating: B-B
- **Stage:** Batch content planning + scheduling
- **What it does:** Generate a full week of social media content for any topic. Platform-optimized posts for Twitter/X, LinkedIn, and Instagram.
- **Key features:**
  - 7-day content calendar generation
  - Platform-optimized posts (LinkedIn, X, Instagram)
  - Hashtag strategies per platform
  - Optimal posting times
  - Topic variation to avoid repetition
- **Use case:** Instead of writing LinkedIn posts one at a time, batch-generate a full week. Give it your blog topics for the week, it creates daily LinkedIn posts, X threads, and Instagram captions — all platform-optimized with posting schedules.
- **Security:** LOW RISK. Content generation only. No API calls. No scheduling service integration (you post manually or connect to Buffer/Hootsuite separately).
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/social-media-scheduler && cp SKILL.md ~/.claude/skills/social-media-scheduler/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/social-media-scheduler && cp SKILL.md ~/.codex/skills/social-media-scheduler/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/social-media-scheduler && cp SKILL.md ~/.openclaw/skills/social-media-scheduler/SKILL.md`

---

### 9. AI Pattern Detection — Score: 8.4/10

- **URL:** https://www.skillhub.club/skills/jmagly-ai-writing-guide-ai-pattern-detection
- **Author:** @jmagly | Tries: 102 | Rating: A 7.8
- **Stage:** Content quality / AI detection avoidance
- **What it does:** Scans text for AI-generated patterns — corporate buzzwords, formulaic transitions, hedging language — and suggests authentic alternatives.
- **Key features:**
  - Detects AI writing patterns (filler phrases, generic transitions, hedge words)
  - Suggests authentic, human-sounding alternatives
  - Pattern library of common AI tells
  - Before/after comparisons
- **Use case:** The quality gate before publishing. Run every blog post and LinkedIn post through this after Content Engine writes it and Voice-Matched Content styles it. Catches the remaining "as we delve into" and "it's worth noting that" patterns that scream AI-generated.
- **Security:** LOW RISK. Text analysis only. No external calls. No API keys. No data sent anywhere.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/ai-pattern-detection && cp SKILL.md ~/.claude/skills/ai-pattern-detection/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/ai-pattern-detection && cp SKILL.md ~/.codex/skills/ai-pattern-detection/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/ai-pattern-detection && cp SKILL.md ~/.openclaw/skills/ai-pattern-detection/SKILL.md`

---

### 10. Rank Tracker — Score: 8.3/10

- **URL:** https://www.skillhub.club/skills/openclaw-skills-rank-tracker
- **Author:** @openclaw | Tries: 3.5k | Rating: B-B
- **Stage:** SEO analytics / rank monitoring
- **What it does:** Track keyword ranking positions and SERP changes over time in both traditional and AI-generated search results.
- **Key features:**
  - Keyword position tracking over time
  - SERP change detection
  - AI search result tracking (ChatGPT, Perplexity, Claude)
  - Ranking trend analysis
- **Use case:** Close the loop. After publishing blog posts, track which keywords you're ranking for and whether positions are improving. Also monitors AI search — are ChatGPT/Perplexity citing your content? Run weekly to measure the impact of your content pipeline.
- **Security:** LOW RISK. Web search queries for ranking data. No API keys required for basic usage. No data exfiltration.
- **Install:**
  - Claude: `mkdir -p ~/.claude/skills/rank-tracker && cp SKILL.md ~/.claude/skills/rank-tracker/SKILL.md`
  - Codex: `mkdir -p ~/.codex/skills/rank-tracker && cp SKILL.md ~/.codex/skills/rank-tracker/SKILL.md`
  - OpenClaw: `mkdir -p ~/.openclaw/skills/rank-tracker && cp SKILL.md ~/.openclaw/skills/rank-tracker/SKILL.md`

---

## Security Overview

| # | Skill | Risk Level | Key Concern |
|---|-------|-----------|-------------|
| 1 | Content Engine | LOW | None — web research + content generation |
| 2 | SEO Audit | LOW | None — analyzes your own site |
| 3 | SEO Research Master | LOW | None — web research only |
| 4 | Programmatic SEO | LOW | None — template-based generation |
| 5 | Voice-Matched Content | LOW | None — analyzes your own content locally |
| 6 | Social Media Post | LOW | None — pure content generation |
| 7 | WordPress Publisher | MEDIUM | WordPress API credentials — use env vars, limit scope |
| 8 | Social Media Scheduler | LOW | None — no external service integration |
| 9 | AI Pattern Detection | LOW | None — text analysis only |
| 10 | Rank Tracker | LOW | None — web search queries only |

**General rule:** Always `grep -iE "(curl|wget|fetch|\.ssh|\.env|credentials|eval|exec|base64)" SKILL.md` before installing any skill.

---

## Honorable Mentions

| Skill | URL | Why it's worth noting |
|-------|-----|----------------------|
| **Copy Editing** | [link](https://www.skillhub.club/skills/coreyhaines31-marketingskills-copy-editing) | 17.3k tries — systematic multi-pass content editing |
| **Purple Cow Content** | [link](https://www.skillhub.club/skills/openclaw-skills-purple-cow-content) | MrBeast + Purple Cow methodology for viral content |
| **Schema Markup** | [link](https://www.skillhub.club/skills/aitytech-agentkits-marketing-schema-markup) | JSON-LD structured data for rich snippets |
| **Link Building** | [link](https://www.skillhub.club/skills/kostja94-marketing-skills-link-building) | Off-page SEO — guest posting, broken link building |
| **GEO Structured Writer** | [link](https://www.skillhub.club/skills/openclaw-skills-geo-structured-writer) | Optimize content for AI search citation |
| **AI Search Optimization** | [link](https://www.skillhub.club/skills/vasilyu1983-ai-agents-public-marketing-ai-search-optimization) | Rating A 8.4 — modern SERP + AI search visibility |
| **Content Marketing** | [link](https://www.skillhub.club/skills/refoundai-lenny-skills-content-marketing) | Full content marketing strategy framework |
| **Growth Hacker** | [link](https://www.skillhub.club/skills/kasperjunge-agent-resources-growth-hacker) | Sean Ellis + Nikita Bier growth frameworks |
| **LinkedIn Announcement** | [link](https://www.skillhub.club/skills/dmccreary-claude-skills-linkedin-announcement-generator) | LinkedIn-specific announcement formatting |
| **Image Studio** | [link](https://www.skillhub.club/skills/openclaw-skills-image-studio) | AI image prompts for blog headers + social visuals |

---

## Quick Start: Recommended Install Order

1. Install **SEO Audit** → diagnose current site health
2. Install **SEO Research Master** → find keywords and content gaps
3. Install **Voice-Matched Content** → extract your brand voice
4. Install **Content Engine** → write SEO-optimized blog posts in your voice
5. Install **AI Pattern Detection** → quality gate before publishing
6. Install **WordPress Publisher** → push posts live
7. Install **Social Media Post** + **Social Media Scheduler** → distribute on LinkedIn/X
8. Install **Rank Tracker** → monitor results and iterate
