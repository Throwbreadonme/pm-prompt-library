# Discovery Prompts

Prompts for the messy, uncertain early stages of product work understanding users, stress-testing assumptions, and framing opportunities before you commit to a solution.

---

## Mock User Interview

**When to use:** Before talking to real users, to stress-test your interview guide and spot leading questions. Also useful when you cannot get user access quickly and need to pressure-test assumptions.

```
You are a [user persona: e.g. "a freelance graphic designer who creates content for social media clients"]. 

I am a product manager running a user research session. I will ask you questions about your experience with [topic/problem area]. 

Stay in character throughout. Answer as this person would: with their priorities, frustrations, vocabulary, and blind spots. Do not give me the answers you think I want. Push back if my questions are leading. Tell me when something does not match your experience.

My first question: [your opening question]
```

**How to adapt:**
- Make the persona as specific as possible job title, context, and one key frustration gets you much further than a generic description
- After the interview, ask: "Where were my questions leading? What did I assume that this user would not?"
- Run the same persona with different emotional states (frustrated, time-pressured, first-time user) to stress-test edge cases

---

## Assumption Mapper

**When to use:** When you have a product idea or proposed solution and want to surface what you are taking for granted before investing in discovery or build.

```
I am working on the following product idea or initiative:

[Describe the idea, feature, or solution in 2–4 sentences]

Help me map my assumptions. For each assumption, indicate:
1. How critical it is to the success of this idea (high / medium / low)
2. How confident I should be that it is true, based on what I have told you (high / medium / low)

Organise them from most critical + least validated to least critical + most validated. Flag any assumptions I may have missed.
```

**How to adapt:**
- Feed in your current evidence for each assumption and ask Claude to update the confidence scores
- Use the output to prioritise what to validate first start with high criticality, low confidence

---

## Opportunity Framing

**When to use:** When you have a user problem or a piece of research and want to frame it as a product opportunity before taking it to stakeholders or into ideation.

```
Here is a user problem or insight I have identified:

[Describe what you learned from research, support tickets, data, or stakeholder input]

Help me frame this as a product opportunity. Include:
1. The underlying user need (not the surface request)
2. Who is most affected and when
3. What a good solution would need to be true
4. What I still do not know and should validate before acting

Be direct if the evidence I have described is thin or if the problem is unclear.
```

**How to adapt:**
- Paste in raw user interview notes or support ticket examples to get a more grounded output
- Ask Claude to steelman the opposite view why this might not be a real opportunity worth pursuing

---

## Jobs To Be Done Extractor

**When to use:** When users are asking for a specific feature or solution and you want to get underneath it to the actual job they are trying to do.

```
Users are asking for [specific feature request or solution].

Help me identify the underlying job to be done. Consider:
- What are they trying to accomplish when they reach for this?
- What would "done" look like for them?
- What are they using today instead, and why is it falling short?
- Are there different user segments who might have different underlying jobs?

Do not assume the feature they asked for is the right solution. Focus on the job.
```
