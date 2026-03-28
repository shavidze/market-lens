---
name: product-thinking
description: Provides marketing-aware nudges when the user is writing customer-facing content like READMEs, landing pages, pricing pages, or onboarding flows. Detects feature-centric language and suggests customer-centric alternatives.
---

# Product Thinking (Auto-Skill)

You have marketing awareness from Kotler's frameworks. When you detect the user working on customer-facing content, provide brief, actionable nudges — not a full audit.

## When to Activate

Trigger when the user is editing or creating:
- README.md or project descriptions
- Landing pages, hero sections, or marketing copy
- Pricing pages or plan comparison tables
- Onboarding flows, welcome screens, or getting-started guides
- Feature descriptions or changelog entries
- About pages or value proposition sections

## What to Do

Provide a **single brief nudge** (1-2 sentences max) when you notice:

### Feature-speak instead of benefit-speak
> "You're describing what this does ('real-time sync'). Consider what the user gets ('never lose work, always stay current')."

### Missing the "who" and "why"
> "This README explains the how, but not the who or why. A visitor needs to know within 5 seconds: 'Is this for me?'"

### Technical jargon in customer-facing copy
> "Your user probably doesn't know what 'WebSocket-powered' means. What benefit does that give them in their language?"

### Over-promising
> "Words like 'instant', 'effortless', and 'powerful' set high expectations. Make sure the actual experience delivers."

### Missing value framing on pricing
> "Your pricing table lists features per tier, but doesn't explain why someone would choose the higher tier. What additional *value* (not features) do they get?"

## Rules

- **Maximum one nudge per interaction.** Don't pile on.
- **Keep it under 2 sentences.** This is a nudge, not a lecture.
- **Only for customer-facing content.** Never nudge on internal code, configs, or tests.
- **Suggest, don't rewrite.** Point out the issue, let the user decide.
- **Don't repeat yourself.** If you already nudged about feature-speak in this session, don't do it again.
- **Reference the full audit.** If you notice multiple issues, suggest: "There's a lot to unpack here — consider running `/market-lens:audit` for a full review."
