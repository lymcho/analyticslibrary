# AI Analytics Prompt Library for Product Teams

**Audience:** PMs and product leaders in B2B SaaS / data-heavy products.
**Goal:** Turn metrics + dashboards into decisions, narratives, and product ideas using LLMs.

Use these prompts as starting points. Always plug in your own context (metrics, segments, time ranges, product details).

---

## 0. How to Use This Library

When you paste a prompt into your LLM (ChatGPT, Claude, internal model):

1. **Add context**
   - What product / feature are we talking about?
   - What time period? Which segment?
   - Any known events (launches, outages, campaigns)?

2. **Paste data in a structured way**
   - Tables copied from dashboards
   - Key numbers (e.g., signup → activation → retention, week-over-week changes)
   - Short bullet notes from you / the team

3. **Be explicit about the output**
   - Ask for bullets, a narrative, or a table.
   - Ask for decision-oriented output ("What should we do next?").

You can also chain prompts: use one prompt to explore, then a second to turn it into a plan.

---

## 1. Weekly Metrics Review Copilot

### 1.1 High-level weekly review

**Prompt:**

> You are an experienced product and analytics partner.
> I will paste the last 4–8 weeks of key product metrics, with week labels and values.
>
> 1. Identify the top 3–5 movements this week (up or down), ranked by impact.
> 2. For each movement, explain possible causes using only the data and context I provide.
> 3. Flag any metrics that look noisy vs. meaningful (e.g., small base, seasonal patterns).
> 4. Suggest 3–5 follow-up questions or slices that would help validate your hypotheses.
>
> Return your answer in this structure:
> - Summary (3 bullets)
> - Top movements (table: metric, change, hypothesis, confidence 1–5)
> - Follow-up questions
>
> Here is the context and data:
> - Product: [short description]
> - Time period: [e.g., last 6 weeks]
> - Known events: [launches, outages, campaigns]
> - Metrics table:
>   [paste table here]

---

### 1.2 Weekly review for a specific funnel

**Prompt:**

> You are a product analyst focused on funnel performance.
> I will give you a funnel (steps and definitions), and recent performance data.
>
> 1. Identify which step(s) changed the most this week.
> 2. Explain how those changes affect the overall conversion and business outcome.
> 3. Propose 2–3 hypotheses for why those steps changed.
> 4. Suggest 2 experiments or changes to test next week.
>
> Output:
> - Short narrative (max 5 bullets)
> - Table: funnel step, last week %, this week %, delta, notes
> - Experiment ideas (each with: hypothesis, metric to move, simple design)
>
> Here is the funnel and data:
> - Funnel definition: [steps + what each means]
> - Data (by week or segment):
>   [paste table here]

---

## 2. Root Cause Analysis ("Why did X move?")

### 2.1 Metric moved, find drivers

**Prompt:**

> You are helping me debug a metric movement.
> A key metric changed significantly. I will give you metric values over time and a breakdown by segments (e.g., country, plan, device).
>
> 1. Identify which segments contributed most to the change.
> 2. Distinguish between absolute impact and relative % change.
> 3. Propose 3–5 plausible explanations based on the data and any context I provide.
> 4. Suggest what to look at next (additional cuts, related metrics).
>
> Format your output as:
> - High-level explanation (3–5 bullets)
> - Table: segment, last period, this period, abs change, % change, contribution notes
> - Follow-up checks
>
> Context and data:
> - Metric: [name + definition]
> - Time period: [e.g., WoW or MoM]
> - Events: [e.g., launch, pricing change]
> - Segment breakdown:
>   [paste table here]

---

### 2.2 Cohort / retention shift

**Prompt:**

> You are a retention analyst.
> I will paste cohort retention data (e.g., signup week vs. week N retention) and any relevant events.
>
> 1. Identify which cohorts are behaving differently from the historical pattern.
> 2. Explain possible reasons (changes in acquisition mix, product changes, seasonality).
> 3. Suggest which cohorts deserve a deeper dive.
> 4. Recommend 2–3 retention experiments or product changes.
>
> Output:
> - Summary of retention health (3 bullets)
> - Table: cohort, baseline retention, actual retention, deviation, notes
> - Suggested experiments / changes
>
> Data:
> [paste cohort table]

---

## 3. Experiment Results Analyzer

### 3.1 Classic A/B test analysis

**Prompt:**

> You are an experiment review partner.
> I will provide the setup and results of an A/B test.
>
> 1. Restate the hypothesis in your own words.
> 2. Summarize the results clearly for a non-technical stakeholder.
> 3. Comment on statistical reliability only using the numbers I provide (do not invent stats).
> 4. Explain business impact in simple terms.
> 5. Recommend whether to: ship, iterate, or discard.
>
> Output:
> - One-paragraph summary
> - Bullet list: pros, cons, risks
> - Recommendation with rationale
>
> Here is the experiment info:
> - Hypothesis:
> - Variant descriptions:
> - Primary metric(s):
> - Results (control vs. treatment):
>   [paste table]
> - Any caveats:

---

### 3.2 Multi-metric tradeoff review

**Prompt:**

> You are a PM weighing tradeoffs in an experiment.
> I will provide experiment results across several metrics (e.g., activation, engagement, revenue, support tickets).
>
> 1. Highlight where the variant wins and where it loses.
> 2. Identify any concerning regressions and how severe they are.
> 3. Explain the tradeoffs in business terms.
> 4. Suggest mitigations if we decide to ship.
>
> Output:
> - Tradeoff summary (3–6 bullets)
> - Table: metric, control, variant, delta, severity (low/med/high)
> - Ship decision suggestion + mitigations
>
> Data:
> [paste table]

---

## 4. Scenario Planning & Forecasting

### 4.1 Simple scenario exploration

**Prompt:**

> You are a strategic partner helping me think through scenarios.
> I will describe a few levers (e.g., activation rate, expansion, churn) and our current baseline.
>
> 1. Propose 3 concrete scenarios (conservative, base, upside) with qualitative descriptions.
> 2. For each scenario, outline what would need to be true for it to happen.
> 3. List 3 levers we can influence and plausible ranges.
> 4. Suggest the 1–2 levers most worth focusing on.
>
> Output:
> - Scenario table: name, description, key assumptions
> - Lever table: lever, current value, plausible range, impact notes
>
> Context:
> - Business model:
> - Current metrics:
> - Time horizon:

---

### 4.2 Team planning for next quarter

**Prompt:**

> You are helping me plan next quarter’s focus areas.
> I will give you:
> - Current key metrics and trends
> - High-level company goals
> - A list of possible initiatives
>
> 1. Group initiatives into 2–3 themes.
> 2. Map each initiative to metrics it is likely to move.
> 3. Suggest a simple prioritization (high/med/low) with rationale.
> 4. Propose 1–2 alternative plans (e.g., focus on depth vs breadth).
>
> Output:
> - Themes with initiatives under each
> - Table: initiative, target metrics, priority, rationale
> - Two alternative plan narratives
>
> Context & inputs:
> [paste goals, metrics, initiatives]

---

## 5. Narrative & Stakeholder Storytelling

### 5.1 Turn metrics into an exec narrative

**Prompt:**

> You are a product leader preparing for an executive review.
> I will provide key metrics, trends, and a bit of context about what happened this period.
>
> 1. Write a concise narrative suitable for a 1–2 slide summary.
> 2. Structure it as: what happened, why it matters, and what we’re doing next.
> 3. Highlight 2–3 key charts we should show and what to say about each.
>
> Output:
> - 3–5 bullet executive summary
> - Suggested slide structure (Slide 1, Slide 2, Slide 3)
> - Notes/script for each slide
>
> Data & context:
> [paste here]

---

### 5.2 Translate analysis into an email / doc update

**Prompt:**

> You are helping me write an update for stakeholders.
> I will paste:
> - Raw analysis notes
> - Key numbers and charts (described in text)
>
> 1. Turn this into a clear written update (email or doc section).
> 2. Keep it scannable, with headings and bullets.
> 3. End with a short "What’s next" section.
>
> Output:
> - Subject line / title
> - Body with headings and bullets
>
> Here are my notes:
> [paste notes]

---

## 6. Designing User-Facing Analytics Copilots

### 6.1 Define the copilot’s responsibilities

**Prompt:**

> You are a product designer defining an analytics copilot.
> I will describe the product, users, and the analytics available.
>
> 1. Propose 5–10 concrete jobs this copilot should do for the user (e.g., weekly summaries, anomaly alerts, "explain this chart").
> 2. For each job, suggest example user questions and copilot responses.
> 3. Highlight what data and context the copilot needs to do this well.
>
> Output:
> - Table: job, user questions, copilot behaviors, required data
>
> Context:
> [describe product, users, data]

---

### 6.2 System prompt for an analytics copilot

**Prompt (system / developer style):**

> You are an analytics copilot helping [user type] understand and act on their data in [product name].
>
> Principles:
> - Be concise and decision-oriented.
> - Explain reasoning using only the data and context provided.
> - Avoid guessing or hallucinating metrics.
> - When data is insufficient, say so and suggest what else is needed.
>
> Capabilities:
> - Summarize trends and changes in key metrics.
> - Compare segments, cohorts, and time periods.
> - Explain possible reasons for changes, with uncertainty called out.
> - Suggest next steps (experiments, deeper dives, actions).
>
> Input format:
> - Product context: [text]
> - User goal: [text]
> - Data: [tables / metrics / notes]
>
> Output format:
> - Brief summary (2–4 bullets)
> - Optional table(s) if helpful
> - Next steps (2–3 bullets)

You can adapt this system prompt verbatim into your own product and extend it with product-specific rules.

---

## 7. Plug-and-Play Flows

These are mini "recipes" you can use as-is or adapt into your own docs.

### 7.1 Weekly product review ritual

1. Export or screenshot your key weekly metrics.
2. Paste them into your LLM with the **Weekly metrics review** prompt (1.1).
3. Ask the model to generate:
   - A 3-bullet summary for leadership
   - A longer internal note for the product team
4. Copy/paste into your weekly doc or Slack update.

---

### 7.2 New feature launch follow-up

**Prompt:**

> You are helping me review the first 2–4 weeks after a feature launch.
> I will provide:
> - Feature description and target users
> - Rollout timeline
> - Key metrics before and after launch
>
> 1. Summarize adoption and impact.
> 2. Highlight any unexpected changes.
> 3. Suggest how to iterate: what to double down on, what to fix.
>
> Output:
> - Launch recap (narrative)
> - Table: metric, before, after, delta, notes
> - Next steps
>
> Data and context:
> [paste here]

---

### 7.3 Churn / downgrade investigation

Use the **Root cause** prompts (2.1, 2.2) with:

- Churned vs. retained cohorts
- Segment breakdowns (plan, geography, company size)

Ask explicitly:

> After analyzing, suggest 2–3 specific interventions to test to reduce churn, with the metric each is expected to move.

---

This library is a starting point. Duplicate, tweak, and remix prompts so they sound like you and fit your product.
