---
layout: default
title: AI Analytics Prompt Library
---

# AI Analytics Prompt Library

**Copy-paste prompts that turn your dashboards into decisions.**

Product teams drown in metrics but starve for insight. This library gives you ready-to-use LLM prompts that transform raw data into weekly summaries, root-cause analyses, experiment reviews, exec narratives, and more -- in minutes instead of hours.

---

## The Problem

You open your dashboard on Monday morning. Numbers everywhere. Some are up, some are down. You know you need to write a summary, figure out *why* activation dropped, and prep slides for Thursday's exec review.

So you stare at charts. Copy numbers into a doc. Try to write something coherent. Two hours later you have a mediocre update.

**This library fixes that.**

---

## How It Works

1. **Pick a prompt** for your task (weekly review, root-cause analysis, experiment results, etc.)
2. **Paste your data** -- a table from your dashboard, key metrics, context about recent launches
3. **Run it** in ChatGPT, Claude, or any LLM
4. **Get structured output** -- summaries, tables, hypotheses, next steps -- ready to drop into docs, decks, or Slack

---

## Example: Weekly Metrics Review

**You paste this into your LLM:**

> You are an experienced product and analytics partner. I will paste the last 4-8 weeks of key product metrics.
>
> 1. Identify the top 3-5 movements this week, ranked by impact.
> 2. For each movement, explain possible causes using only the data I provide.
> 3. Flag any metrics that look noisy vs. meaningful.
> 4. Suggest 3-5 follow-up questions to validate your hypotheses.
>
> **Product:** B2B project management tool  
> **Time period:** Last 6 weeks  
> **Known events:** Launched new onboarding flow in Week 4  
>
> | Metric | W1 | W2 | W3 | W4 | W5 | W6 |
> |---|---|---|---|---|---|---|
> | Signups | 1,200 | 1,180 | 1,210 | 1,350 | 1,420 | 1,390 |
> | Activation (7d) | 34% | 33% | 35% | 41% | 43% | 42% |
> | WAU | 8,500 | 8,400 | 8,550 | 8,900 | 9,100 | 9,050 |
> | Churn rate | 4.2% | 4.1% | 4.3% | 4.0% | 3.8% | 3.9% |

**You get back:**

> **Summary**
> - Activation jumped +8pp after the new onboarding flow launched in W4 and has held steady, suggesting a real improvement rather than noise.
> - Signups are up ~15% over the period, likely driven by the same launch (better early experience → word of mouth) but could also reflect a separate acquisition push.
> - Churn ticked down modestly; too early to attribute to onboarding but worth watching.
>
> **Top Movements**
>
> | Metric | Change | Hypothesis | Confidence |
> |---|---|---|---|
> | Activation | +8pp (W3→W4) | New onboarding flow | 4/5 |
> | Signups | +12% (W3→W4) | Onboarding buzz or separate campaign | 2/5 |
> | Churn | -0.4pp (W3→W6) | Early signal from better activation | 2/5 |
>
> **Follow-up Questions**
> 1. Can we segment activation by onboarding version (old vs new)?
> 2. What drove the signup increase -- organic, paid, or referral?
> 3. Are the newly activated users retaining at the same rate as before?

---

## What's Inside

The full library covers seven areas:

| Category | What It Does |
|---|---|
| **Weekly Metrics Review** | Turn your Monday dashboard export into a clear, prioritized summary with hypotheses |
| **Root Cause Analysis** | Debug "why did this metric move?" with structured segment breakdowns |
| **Experiment Analysis** | Translate A/B test results into ship/iterate/kill decisions |
| **Scenario Planning** | Explore conservative/base/upside paths for quarterly planning |
| **Stakeholder Storytelling** | Convert raw analysis into exec summaries, email updates, and slide narratives |
| **Copilot Design** | Define and prompt user-facing analytics copilots for your own product |
| **Plug-and-Play Flows** | Drop-in rituals for weekly reviews, launch follow-ups, and churn investigations |

---

## Who This Is For

- **Product managers** who spend too long turning dashboards into updates
- **Product leaders** who need to prep exec reviews from messy data
- **Growth / analytics PMs** who run experiments and need fast, structured readouts
- **Teams building analytics features** who want to design AI copilots on top of their data

---

## Get the Prompts

The full prompt library lives on GitHub -- every prompt is copy-paste ready:

[**View the full prompt library on GitHub →**](https://github.com/lymcho/analyticslibrary/blob/main/product/prompt-library.md)

---

## Pricing: Free / Pay What You Want

Everything here is free to use, remix, and share with your team.

If this library saves you real time or becomes part of your workflow, you can send a tip:

- **Venmo:** `@YOUR_VENMO`

Tips are optional. They help justify maintaining and expanding the library.

---

## Feedback

Have a workflow you'd like prompts for? Found something that could be better?

[Open an issue on GitHub](https://github.com/lymcho/analyticslibrary/issues) or submit a pull request.
