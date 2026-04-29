# Data Interpretation Prompts

Prompts for making sense of metrics not just reading what the numbers say, but challenging your own interpretation and finding the signal in the noise.

---

## Sense-Check My Read

**When to use:** When you have looked at a set of metrics and formed a hypothesis, and you want to pressure-test your interpretation before sharing it with stakeholders or acting on it.

```
I am looking at the following data or metrics:

[Paste your data, chart description, or summary of what you are seeing]

My current interpretation is:

[Describe what you think is happening and why]

Challenge my interpretation. What alternative explanations could account for the same data? What am I potentially missing, over-indexing on, or confusing for causation when it might be correlation? What would I need to see to feel more confident in my read?
```

**How to adapt:**
- Include the time period, cohort, and any recent product changes that might be confounders
- Ask Claude to suggest the one additional data point that would most help resolve the ambiguity

---

## Metric Drop Investigation

**When to use:** When a key metric has dropped and you need to structure your investigation before pulling more data.

```
A key metric has dropped. Here is what I know:

Metric: [e.g. D7 retention, lesson completion rate, activation rate]
Drop: [e.g. from 42% to 36% over the last two weeks]
Context: [Any recent changes releases, experiments, seasonal factors, data pipeline issues]

Help me build a structured investigation plan. What are the most likely causes, ordered by probability? What data would I pull first to narrow it down? What would rule out each hypothesis?
```

**How to adapt:**
- Update with what you find at each step and ask Claude to revise the hypothesis list
- Ask: "What is the most boring explanation?" often the right one

---

## Experiment Results Interpreter

**When to use:** After an A/B test, to think through what the results actually mean before declaring a winner or loser.

```
Here are the results of an experiment I ran:

Hypothesis: [What you were trying to prove]
Variant: [What you changed]
Primary metric: [Result e.g. +3% D7 retention, p=0.04]
Secondary metrics: [Any guardrail or secondary metrics and their results]
Sample size and duration: [e.g. 50k users, 3 weeks]

Help me think through what these results actually mean. Is the primary metric result meaningful? Are there any concerns with the secondary metrics? What would ship vs. no-ship look like, and what would I want to be true before I shipped? What should I be cautious about?
```

**How to adapt:**
- Include any segment breakdowns (new vs. returning users, markets, device types) that showed different patterns
- Ask: "What is the strongest argument for not shipping this?"

---

## North Star Alignment Check

**When to use:** When you are deciding which metrics to track for a new initiative and want to make sure they connect to outcomes that actually matter.

```
I am working on [initiative or feature]. 

Here are the metrics I am planning to track:

[List your proposed metrics]

Help me evaluate whether these metrics are well-chosen. For each one:
1. Does it measure an outcome or a behaviour? (Outcome is better)
2. Could it be gamed or move for the wrong reasons?
3. How closely does it connect to the north star metric or business outcome?

Suggest any metrics I am missing and flag any I should drop or reframe.
```
