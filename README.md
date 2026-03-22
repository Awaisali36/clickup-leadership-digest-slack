# Automated Weekly ClickUp Leadership Digest → Slack
### Every Monday at 8 AM. Every Project. Zero Manual Effort.

<div align="center">

![Type](https://img.shields.io/badge/Type-Delivered%20Client%20System-%233A7CFF?style=for-the-badge)
&nbsp;
![Speed](https://img.shields.io/badge/80%20min%20→%2030%20sec-97%25%20Faster-%2300C853?style=for-the-badge)
&nbsp;
![Leaders](https://img.shields.io/badge/Reaches-10–20%20Leaders-%23FF6B35?style=for-the-badge)

</div>

<br/>

---

## What This Is

An automated weekly reporting system built for **Reprise AI** — every Monday at 8 AM, it pulls all ClickUp tasks updated in the last 7 days, categorizes project health, generates an executive-ready summary using Claude AI, and delivers a structured digest with stats dashboard and drill-down links directly to Slack.

Leadership has full project visibility before the week begins. No meetings. No manual reporting. No delays.

<br/>

---

## Why This Matters

> A leadership team that's always one week behind on project status isn't leading — it's reacting.

Weekly reporting exists for one reason: to give decision-makers the information they need to act. But when that report takes 80 minutes to compile manually, it happens inconsistently, arrives late, and gets written by someone who should be doing something else.

```
  80 minutes × 52 weeks
= 69 hours of leadership time spent on data collection per year

  10–20 leaders waiting for the report to arrive
= Delayed decisions. Missed escalations. Status meetings that
  could have been a Slack message.

  Manual categorization of tasks into status buckets
= Subjective. Inconsistent. Dependent on who wrote it that week.
```

Automating the digest doesn't just save time — it makes the report **more reliable, more consistent, and available exactly when it's needed.**

<br/>

---

## Before vs. After

```
╔══════════════════════════════════════════════════════════════════╗
║                        BEFORE                                    ║
╠══════════════════════════════════════════════════════════════════╣
║                                                                  ║
║  Monday morning                                                  ║
║       │                                                          ║
║       ▼                                                          ║
║  Someone logs into ClickUp manually            ← 5 min           ║
║       │                                                          ║
║       ▼                                                          ║
║  Filters tasks updated in last 7 days          ← 10 min          ║
║       │                                                          ║
║       ▼                                                          ║
║  Manually categorizes: done / at risk / ok     ← 20 min          ║
║       │                                                          ║
║       ▼                                                          ║
║  Writes executive summary paragraph            ← 20 min          ║
║       │                                                          ║
║       ▼                                                          ║
║  Formats and posts to Slack                    ← 10 min          ║
║       │                                                          ║
║       ▼                                                          ║
║  Adds links and stats manually                 ← 15 min          ║
║                                                                  ║
║  TOTAL: 80 minutes   CONSISTENCY: Variable   TIMING: Whenever   ║
╚══════════════════════════════════════════════════════════════════╝


╔══════════════════════════════════════════════════════════════════╗
║                         AFTER                                    ║
╠══════════════════════════════════════════════════════════════════╣
║                                                                  ║
║  Monday 8:00 AM — trigger fires automatically                    ║
║       │                                                          ║
║       ├──► ClickUp API pulls all tasks (last 7 days) ← 2 sec     ║
║       ├──► Categorization logic runs               ← 1 sec       ║
║       ├──► Claude AI generates executive summary   ← 8 sec       ║
║       ├──► Stats dashboard compiled               ← 1 sec        ║
║       └──► Full digest posted to Slack            ← 0.5 sec      ║
║                                                                  ║
║  TOTAL: 30 seconds   CONSISTENCY: Perfect   TIMING: Always 8 AM ║
╚══════════════════════════════════════════════════════════════════╝
```

<br/>

---

## How It Works

```
┌──────────────────────────────────────────────────────────────────┐
│               MONDAY 8:00 AM — CRON TRIGGER                      │
└──────────────────────────┬───────────────────────────────────────┘
                           │
                           ▼
              ClickUp API — pull all tasks
              updated in last 7 days
              across entire workspace
                           │
                           ▼
┌──────────────────────────────────────────────────────────────────┐
│                  CATEGORIZATION ENGINE                           │
│                                                                  │
│   ✅ COMPLETED    Tasks marked done this week                    │
│   ⚠️  AT RISK     Overdue · blocked · no update in 5+ days       │
│   ✅ ON TRACK     Active · updated · within deadline             │
└──────────┬───────────────┬────────────────────┬─────────────────┘
           ▼               ▼                    ▼
     Count + list    Count + list          Count + list
     with client     with client           with client
     names & URLs    names & URLs          names & URLs
           │               │                    │
           └───────────────┴────────────────────┘
                           │
                           ▼
              Claude AI — generate 3-paragraph
              executive summary:
              Para 1: Overall project health
              Para 2: Key wins this week
              Para 3: Items needing attention
                           │
                           ▼
┌──────────────────────────────────────────────────────────────────┐
│                    SLACK DIGEST POSTED                           │
│                                                                  │
│   📊 Quick Stats Dashboard                                       │
│      X completed · X at risk · X on track                       │
│                                                                  │
│   🧠 AI Executive Summary (3 paragraphs)                         │
│                                                                  │
│   📋 Detailed Breakdown                                          │
│      Each category with client names + ClickUp URLs             │
└──────────────────────────────────────────────────────────────────┘
```

<br/>

---

## What the Slack Digest Looks Like

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📊 WEEKLY PROJECT DIGEST — Mon 17 Mar 2025
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

QUICK STATS
✅  Completed this week:    12 tasks
⚠️   At risk:                3 tasks
🟢  On track:               28 tasks

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🧠 EXECUTIVE SUMMARY
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[Paragraph 1 — Overall health across all projects]
[Paragraph 2 — Key completions and wins this week]
[Paragraph 3 — Items requiring leadership attention]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📋 AT RISK — Needs Attention
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

• Client A — Task Name → [ClickUp link]
• Client B — Task Name → [ClickUp link]
• Client C — Task Name → [ClickUp link]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
✅ COMPLETED THIS WEEK
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

• Client D — Task Name → [ClickUp link]
• Client E — Task Name → [ClickUp link]
... and 10 more
```

<br/>

---

## Results

| Metric | Before | After |
|---|---|---|
| Weekly reporting time | **80 minutes** | **30 seconds** |
| Time saved per year | — | **69 hours** |
| Report consistency | Variable | **Perfect — every Monday** |
| Delivery time | Whenever someone gets to it | **8:00 AM sharp** |
| Leaders receiving digest | 10–20 | **10–20 (always, never missed)** |
| Status meetings replaced | — | **Measurable reduction** |
| Subjective categorization risk | Present | **Zero — logic-based** |

<br/>

---

## Tech Stack

| Layer | Tool | Purpose |
|---|---|---|
| **Orchestration** | n8n | Workflow automation and Monday 8 AM scheduling |
| **Data Source** | ClickUp API | Task extraction across full workspace |
| **Categorization** | Custom logic | Completed / At Risk / On Track bucketing |
| **Summary AI** | Claude AI | Executive 3-paragraph summary generation |
| **Delivery** | Slack API | Formatted digest with stats and drill-down links |

<br/>

---

## Repository Structure

```
📁 clickup-leadership-digest-slack/
├── 📄 README.md
├── 📁 workflow/
│   └── leadership-digest.json         ← n8n workflow export
├── 📁 prompts/
│   └── claude-summary-prompt.md       ← Claude AI prompt
└── 📁 docs/
    └── categorization-logic.md        ← Task bucketing rules
```

<br/>

---

## Built by Trilles AI

This system was designed and delivered by **[Awais Ali](https://www.linkedin.com/in/awais-ali-tillesai)**, CEO & Co-Founder of **[Trilles AI](https://www.trillesai.com)**.

If your leadership team is still waiting on manual reports to understand what's happening across your projects — this is exactly what we automate.

<div align="center">

[![Connect on LinkedIn](https://img.shields.io/badge/Connect%20on%20LinkedIn-%230A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/awais-ali-tillesai)
&nbsp;
[![Visit Trilles AI](https://img.shields.io/badge/Visit%20Trilles%20AI-%233A7CFF?style=for-the-badge&logoColor=white)](https://www.trillesai.com)
&nbsp;
[![Email](https://img.shields.io/badge/Email%20Me-%23EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:letsautomatewithawais@gmail.com)

</div>

<br/>

---

<div align="center">
<sub>Built with precision · Powered by Trilles AI · <code>www.trillesai.com</code></sub>
</div>
