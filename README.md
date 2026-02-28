# AI Analytics Prompt Library

**Copy-paste LLM prompts that turn your dashboards and metrics into decisions, narratives, and experiments.**

Product teams spend hours staring at dashboards trying to turn numbers into something useful -- a weekly summary, a root-cause explanation, an exec-ready slide. This library gives you structured prompts you can paste into ChatGPT, Claude, or any LLM along with your data, and get polished, decision-oriented output in minutes.

**Live site:** [https://lymcho.github.io/analyticslibrary](https://lymcho.github.io/analyticslibrary)

---

## What's in the Library

The core product is [`product/prompt-library.md`](product/prompt-library.md) -- a collection of prompts organized by use case:

| Category | Use Case |
|---|---|
| **Weekly Metrics Review** | Paste your weekly numbers, get a prioritized summary with hypotheses and follow-ups |
| **Root Cause Analysis** | A metric moved -- find which segments drove it and why |
| **Experiment Analysis** | Turn A/B test results into a clear ship/iterate/kill recommendation |
| **Scenario Planning** | Model conservative/base/upside paths for quarterly planning |
| **Stakeholder Storytelling** | Convert raw analysis into exec summaries, emails, and slide narratives |
| **Copilot Design** | Define and prompt user-facing analytics copilots for your product |
| **Plug-and-Play Flows** | Drop-in rituals for weekly reviews, launch follow-ups, churn investigations |

---

## Quick Example

Here's how the **weekly metrics review** prompt works in practice.

**You paste this into your LLM:**

> You are an experienced product and analytics partner. I will paste the last 4-8 weeks of key product metrics.
>
> 1. Identify the top 3-5 movements this week, ranked by impact.
> 2. For each, explain possible causes using only the data I provide.
> 3. Flag noisy vs. meaningful signals.
> 4. Suggest 3-5 follow-up questions.
>
> **Product:** B2B project management tool
> **Known events:** Launched new onboarding flow in Week 4
>
> | Metric | W1 | W2 | W3 | W4 | W5 | W6 |
> |---|---|---|---|---|---|---|
> | Signups | 1,200 | 1,180 | 1,210 | 1,350 | 1,420 | 1,390 |
> | Activation (7d) | 34% | 33% | 35% | 41% | 43% | 42% |
> | WAU | 8,500 | 8,400 | 8,550 | 8,900 | 9,100 | 9,050 |

**The LLM returns** a structured summary: activation jumped +8pp after the onboarding launch and held, signups are up 15% but the cause is ambiguous, and here are 5 specific follow-up questions to validate each hypothesis. Ready to paste into your weekly doc.

Every prompt in the library works this way: you bring the data, the prompt gives the LLM the right structure and role, and you get back something you can actually use.

---

## How to Use

1. Open [`product/prompt-library.md`](product/prompt-library.md)
2. Find the section that matches your task
3. Copy the prompt into your LLM
4. Fill in the bracketed placeholders with your own context, metrics, and data
5. Run it and iterate

Each prompt tells the LLM what role to play, what structure to follow, and what output format to use. You customize by plugging in your product context.

---

## Repo Structure

```
analyticslibrary/
├── product/
│   ├── prompt-library.md    ← The full prompt library (core product)
│   └── CHANGELOG.md         ← Version history
├── site/
│   ├── index.md             ← GitHub Pages landing page
│   └── _config.yml          ← Jekyll config
├── .github/
│   └── workflows/
│       └── pages.yml        ← GitHub Pages deployment
└── README.md                ← You are here
```

---

## Landing Page

The `site/` folder contains a Jekyll-based landing page deployed to GitHub Pages at:

**[https://lymcho.github.io/analyticslibrary](https://lymcho.github.io/analyticslibrary)**

It provides a friendlier introduction to the library with examples, and links back to the full prompt library on GitHub.

---

## Support / Pay What You Want

This library is free to use, remix, and share.

If it saves you real time or becomes part of your team's workflow, you can send a tip:

- **Venmo:** `@YOUR_VENMO`

---

## Contributing

Ideas for new prompts? Found something that could be better?

- [Open an issue](https://github.com/lymcho/analyticslibrary/issues)
- Submit a pull request

---

## Changelog

See [`product/CHANGELOG.md`](product/CHANGELOG.md) for version history.
