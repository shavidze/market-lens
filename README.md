# Market Lens

A Claude Code plugin that audits your product through Kotler's marketing lenses. Stop building features nobody asked for — start solving problems people will pay for.

## What It Does

Market Lens challenges you to think about your product from the **customer's perspective**. It scans your codebase, asks pointed questions, and runs you through 4 marketing lenses — acting as a provocative sparring partner, not a polite reviewer.

### The 4 Lenses

| Lens | Question | What It Catches |
|------|----------|-----------------|
| **Myopia Check** | Are you selling the drill or the hole? | Feature-obsession, technical jargon in customer-facing copy |
| **Value Perception** | What does the customer get vs give? | Onboarding friction, hidden costs, unclear value props |
| **Satisfaction Risk** | Where will expectations break? | Over-promises, poor error states, promise-delivery gaps |
| **Retention Signal** | Why would they come back tomorrow? | Missing engagement hooks, one-time-use patterns |

### How It Works

1. **Silently scans** your codebase — README, landing pages, pricing, onboarding, error handling
2. **Asks 3 context questions** — your target user, the problem you solve, the alternatives
3. **Challenges you** lens by lens — presents findings, asks tough questions, pushes back
4. **Generates a report** — `PRODUCT-AUDIT.md` with findings, risk levels, and top 3 action items

## Install

```bash
claude plugin install market-lens
```

Or load locally for development:

```bash
claude --plugin-dir ./market-lens
```

## Usage

### Full Audit (~15 min)
```
/market-lens:audit
```
Interactive 4-lens audit with challenges, pushback, and a final report.

### Quick Check (~3 min)
```
/market-lens:quick
```
Myopia check only — fast gut-check on whether you're building the right thing.

### Auto-Nudges
The `product-thinking` skill activates automatically when you're editing customer-facing content (README, landing pages, pricing). It provides brief marketing-aware nudges without interrupting your flow.

## Example Output

After running `/market-lens:audit`, you get a `PRODUCT-AUDIT.md` like:

```
## Lens 1: Myopia Check 🔴

Finding: Your README opens with "A Next.js application with real-time
WebSocket support and PostgreSQL backend." Your customer doesn't care
about your stack. They care about what problem you solve.

Recommendation: Rewrite your README opening to: "For [target user]
who [has this problem], [Product Name] [solves it by]..."
```

## Who Is This For?

- **Solo founders** building products end-to-end
- **Indie hackers** who code AND market
- **Engineers** shipping features who want to think like product managers
- **Anyone** who believes the next generation of builders needs more than just coding skills

## Based On

Frameworks derived from Philip Kotler's *Principles of Marketing* — adapted for builders who work in code, not boardrooms.

## License

MIT
