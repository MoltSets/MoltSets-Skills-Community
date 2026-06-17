---
name: your-skill-name
description: Use this skill when <the exact situation that should trigger it>. One or two sentences. Write it in the third person ("Use this skill when the user wants to…") and be specific about the inputs the skill needs — this is what Claude reads to decide when to load the skill.
---

# Your Skill Name

<!--
This is the file Claude actually loads. Keep it self-contained: a new Claude
session with no other context should be able to follow it end to end.
Delete every HTML comment before submitting. Keep the section order below —
it matches the rest of the library — but drop any section that genuinely
doesn't apply.
-->

One or two lines on what the skill does and, if it calls tools/MCPs, which ones (e.g. "using `MoltSets:reverse_email_lookup`" or "using the Ahrefs MCP server").

## Triggers

The phrases and situations that should activate this skill — e.g. "find the email for [name] at [company]", "enrich these LinkedIn URLs", "run topic research for [domain]". Also state when NOT to use it, and which skill to use instead.

## Requirements

<!-- Delete if the skill needs nothing beyond Claude itself. -->

- Tools / MCP servers the skill depends on (e.g. MoltSets MCP, Ahrefs MCP)
- Inputs the user must provide (a CSV, a domain, a list of URLs, etc.)

## Steps

Numbered, in order. For each step say which tool to call and with which parameters.

1. **Step name** — what to do, which tool, which params.
2. **Step name** — …
3. …

<!-- If the skill loops over a list, say so explicitly and state any per-call
limits (e.g. "one call per URL" vs "batch array, max 100"). Be precise about
parameter names — wrong names fail silently. -->

## Output

Show the exact shape of what the user gets back — a contact block, a table, a
report. Use a fenced code block or a markdown table so it's unambiguous.

```
Example output here
```

## Edge cases

- What to do when a lookup returns nothing
- Malformed / partial input
- Anything the model should never do (e.g. never fabricate data — only surface what the tool returns)
