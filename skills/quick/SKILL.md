---
name: quick
description: "Quick myopia check — are you building the drill or solving the hole? Fast 3-minute gut-check on your product positioning."
---

# Market Lens: Quick Check

Fast, focused version of the full audit. One lens only: **Myopia Check**.

**Tone:** Same provocative sparring partner as the full audit, but faster. Get to the point in under 5 minutes.

## Reference Files

Before starting, read these files from the plugin directory at `${CLAUDE_PLUGIN_ROOT}`:
- `${CLAUDE_PLUGIN_ROOT}/references/scan-patterns.md` — what to scan in the codebase
- `${CLAUDE_PLUGIN_ROOT}/references/challenges/01-myopia.md` — the myopia challenge script

## Flow

### Step 1: Silent Scan
Read `${CLAUDE_PLUGIN_ROOT}/references/scan-patterns.md` for scan patterns. Then scan the current project's README, package.json, and any landing page / hero component. Look for how the product describes itself — feature-first or problem-first.

### Step 2: One Question
> "In one sentence — what problem does your user have BEFORE they find your product?"

### Step 3: Myopia Challenge
Read `${CLAUDE_PLUGIN_ROOT}/references/challenges/01-myopia.md` and follow its challenge script exactly:

1. Present what you found in the README/landing page
2. Challenge: "Describe your product without mentioning a single feature."
3. Push back on the response if needed
4. Give your finding with risk level

### Step 4: Quick Verdict

End with a single actionable takeaway:

> **🟢/🟡/🔴 Myopia Check:** {one-line finding}
>
> **One thing to do right now:** {specific, immediate action}
>
> Run `/market-lens:audit` for the full 4-lens deep dive.

## Rules
- Total interaction should be under 5 minutes
- Maximum 2 back-and-forth exchanges with the user
- One finding, one recommendation, one action item
- Always provide your recommended answer for each question — the user can accept, reject, or modify
- Always suggest the full audit at the end
