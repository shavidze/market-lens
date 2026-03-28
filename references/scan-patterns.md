# Scan Patterns

What to look for in the codebase before starting the interactive audit. Scan silently — don't overwhelm the user with file listings. Extract insights, not file paths.

## Phase 1: Project Identity

Scan these files to understand what the project is:

| Priority | Glob Pattern | What to Extract |
|----------|-------------|-----------------|
| 1 | `README.md`, `README.*` | Product description, value proposition, tagline |
| 2 | `package.json`, `Cargo.toml`, `pyproject.toml`, `go.mod` | Project name, description, dependencies |
| 3 | `CLAUDE.md`, `.claude/CLAUDE.md` | Project context, conventions |
| 4 | `LICENSE*` | License type (commercial vs open source signals intent) |

## Phase 2: Customer-Facing Copy

Scan for user-visible text — this is where marketing promises live:

| Priority | Glob Pattern | What to Extract |
|----------|-------------|-----------------|
| 1 | `**/index.{html,tsx,jsx,vue,svelte}` | Landing page / homepage copy |
| 2 | `**/{hero,landing,home,marketing}*` | Marketing-specific components |
| 3 | `**/{pricing,plans,billing}*` | Pricing structure, tier names, value framing |
| 4 | `**/{onboarding,welcome,setup,getting-started}*` | First-run experience |
| 5 | `**/{about,features,benefits,why}*` | Value proposition pages |
| 6 | `**/{signup,register,login,auth}*` | Entry friction |
| 7 | `**/{404,error,not-found}*` | Error experience |

## Phase 3: Retention & Engagement Signals

Scan for patterns that indicate retention thinking:

| Priority | Glob Pattern / Grep Pattern | What It Signals |
|----------|----------------------------|-----------------|
| 1 | `**/{email,notification,alert,reminder}*` | Communication with users |
| 2 | `**/{dashboard,profile,settings,preferences}*` | Personalization / returning user experience |
| 3 | `**/{analytics,tracking,metrics,events}*` | User behavior awareness |
| 4 | `**/{feedback,survey,rating,review,nps}*` | Feedback loops |
| 5 | `**/{invite,share,refer,social}*` | Growth / viral mechanisms |
| 6 | `**/{streak,progress,achievement,badge,gamif}*` | Engagement hooks |
| 7 | `**/{changelog,updates,whatsnew}*` | Ongoing relationship signals |

## Phase 4: Quality & Promise-Delivery Gaps

| Priority | Grep Pattern | What It Signals |
|----------|-------------|-----------------|
| 1 | `TODO`, `FIXME`, `HACK`, `XXX` | Known debt visible to users? |
| 2 | `loading`, `spinner`, `skeleton` | Loading state handling |
| 3 | `empty`, `no results`, `no data`, `nothing here` | Empty state handling |
| 4 | `error`, `failed`, `sorry`, `oops` | Error messaging tone |
| 5 | `coming soon`, `beta`, `experimental` | Incomplete feature signals |
| 6 | `disabled`, `readonly`, `locked` | Gated/restricted features |

## Scan Rules

1. **Be fast.** Use Glob first, then Read only the most relevant files. Don't read every match.
2. **Extract meaning, not code.** Pull out user-visible strings, descriptions, headings — not implementation details.
3. **Note what's MISSING.** The absence of pricing pages, onboarding flows, or retention mechanisms is often the most important finding.
4. **Don't report scan results raw.** Synthesize findings into lens-specific insights before presenting to the user.
5. **Prioritize.** If you find 20 files, read the top 5 most relevant. Quality over quantity.
