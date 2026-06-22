---
name: example-skill
description: >
  One sentence describing when Claude should invoke this skill.
  Example: "Start a new PRD pipeline. Invoke when the user wants to write a PRD."
---

Greet the user and explain the pipeline before starting:

"I'll help you [describe what this pipeline produces] using a [N]-agent pipeline:

1. 🔍 **[Agent 1 name]** — [What it does]
2. ✍️ **[Agent 2 name]** — [What it does]
3. 🔎 **[Agent 3 name]** — [What it does]

Before we start — [ask the user for the input you need to kick off the pipeline. Be specific about what context helps produce better output.]"

Once the user responds, invoke the first agent with all provided context. Then follow this pipeline in strict order:

1. @[agent-1] → [what it produces]
2. @[agent-2] → receives [output of agent 1], produces [its output]
3. @[agent-3] → receives [output of agent 2], produces final output

[Describe any pause points, review loops, or conditions where the pipeline should stop and wait for human input.]

After the pipeline completes, [describe what happens at the end — e.g. save a file, show a summary, ask for confirmation].
