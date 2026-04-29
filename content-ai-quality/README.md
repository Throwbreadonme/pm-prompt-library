# Content & AI Quality Prompts

Prompts for evaluating AI-generated content, classifying failure modes, and designing rubrics that make quality measurable. Built from experience shipping AI-assisted content workflows where human judgment still has to be in the loop.

---

## AI Output Quality Review

**When to use:** When you need to evaluate a batch of AI-generated content and want a structured assessment.

```
I need to evaluate the quality of the following AI-generated content.

Context: [What the content is for, who the end user is, and what good looks like]

Content to evaluate:
[Paste the AI-generated content]

Assess the content across the following dimensions:
1. Accuracy is it factually correct and free of hallucination?
2. Clarity is it easy to understand for the intended user?
3. Appropriateness does it match the tone, register, and context?
4. Completeness does it cover what it needs to, without unnecessary padding?
5. [Add any domain-specific dimension relevant to your context]

For each dimension, give a rating (pass / needs revision / fail) and a specific reason. Flag any issues that would require human review before this content reaches a user.
```

**How to adapt:**
- Add domain-specific dimensions (e.g. pedagogical soundness for learning content, legal safety for regulated industries)
- Use the output as a rubric template by asking Claude to generalise the failure patterns it found

---

## Failure Mode Classifier

**When to use:** When you are building a quality classifier or rubric and need to define the categories of failure clearly enough that a model (or a human reviewer) can apply them consistently.

```
I am building a quality classifier for [type of content]. I have identified the following failure modes:

[List your current failure categories, even if rough]

Help me refine these into a clean taxonomy. Each category should be:
- Mutually exclusive (a piece of content should not clearly fit two categories)
- Clearly defined with a one-sentence description
- Accompanied by a concrete example of what it looks like in practice

Flag any failure modes I may have missed based on the content type I described.
```

**How to adapt:**
- Paste in real examples of bad content and ask Claude to classify them against your taxonomy misclassifications reveal where your definitions are ambiguous
- Ask: "Which of these categories is hardest to distinguish from the others, and why?"

---

## Rubric Designer

**When to use:** When you need a scoring rubric for evaluating content, AI outputs, or any work product where quality needs to be assessed consistently across reviewers.

```
I need a scoring rubric for evaluating [type of content or output].

The evaluator will be [who is doing the scoring e.g. a domain expert, a non-specialist reviewer, an LLM].
The content will be used for [end use case].
The most important quality dimension is [your top priority].

Design a rubric with:
- 3–5 dimensions
- A 1–3 or 1–4 scale for each (avoid 5-point scales they introduce too much ambiguity in the middle)
- Clear, behavioural descriptors for each score level (not vague adjectives like "good" or "adequate")
- A worked example for the highest and lowest score on the most important dimension
```

**How to adapt:**
- Test the rubric by asking Claude to score the same piece of content twice with slightly different instructions inconsistency reveals underspecified descriptors
- Ask reviewers to flag every time they are unsure which score to give those are the rubric's weak spots

---

## Human-in-the-Loop Design

**When to use:** When you are designing an AI-assisted workflow and need to decide where humans should stay in the loop and where automation can safely run on its own.

```
I am designing a workflow where AI [describe what the AI is doing].

The output will be used for [end use case], and errors would [describe the consequence of a bad output e.g. reach a user, affect a business decision, be reviewed before publishing].

Help me identify:
1. Which parts of this workflow are safe to automate fully
2. Which parts need a human to review before the output is used
3. What the human reviewer should specifically be checking for (not a generic quality check the specific failure modes that automation is most likely to miss)
4. What signals I could use to triage i.e. route only high-risk outputs to human review rather than everything
```
