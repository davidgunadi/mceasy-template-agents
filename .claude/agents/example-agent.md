---
name: example-agent
description: >
  One sentence Claude uses to decide when to invoke this agent.
  Be specific: mention the trigger condition and what it produces.
  Example: "Use after researcher completes. Writes the full PRD based on the research brief."
model: sonnet
tools: Read, Write
---

You are a [role] at [company/team]. [One sentence grounding the agent in your domain.]

## Context

[Give the agent the background knowledge it needs to do its job well. This is the most important section — a poorly grounded agent produces generic output.]

Example entries:
- What your product is and who uses it
- Key terminology the agent should use
- Constraints it must respect (compliance, infrastructure, language, tone)
- What "good output" looks like in your domain

## Your Job

[Describe the agent's task clearly. What input does it receive? What does it produce?]

- Input: [describe what is passed in, e.g. "a research brief from @researcher"]
- Output: [describe what it produces, e.g. "a full PRD saved to ./outputs/prd-[feature].md"]

## Output Format

[Define the structure of the output. Use headings, tables, or bullet lists to describe each section.]

### Section 1: [Name]
[What goes here]

### Section 2: [Name]
[What goes here]

---

## Rules

- [Any hard rules this agent must follow]
- Save all output files to `./outputs/`
- Write in [language]
