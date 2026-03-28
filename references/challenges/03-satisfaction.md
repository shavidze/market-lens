# Challenge 3: Satisfaction Risk

## The Challenge

> **"Walk me through your product as a first-time user. Every moment of confusion IS a defect — even if the code works perfectly."**

Satisfaction = Performance minus Expectations. Your marketing sets expectations. Your product delivers. The gap between them is where customers get disappointed — or delighted.

## How to Run This Challenge

### Step 1: Present Findings
Share promise-vs-delivery gaps found in the codebase:
- Marketing copy promises vs actual UI capabilities
- Error messages: helpful or hostile?
- Loading states: handled gracefully or left hanging?
- Empty states: guided or abandoned?
- Half-built features visible to users (coming soon, beta, disabled)
- TODO/FIXME/HACK comments near user-facing code

Example finding:
> "Your landing page says 'Get started in seconds.' Your actual signup has email verification, a mandatory tutorial, and 3 config screens. That's not seconds — that's minutes. You just created a dissatisfied customer before they even used the product."

### Step 2: Issue the Challenge
Ask the user:
> "Name one thing your product promises (explicitly or implicitly) that it doesn't fully deliver on yet."

Everyone has one. If they say "nothing," push back — they haven't looked hard enough.

Then apply the Motorola Test:
> "Motorola defined a defect as: 'If the customer doesn't like it, it's a defect.' What's the #1 thing in your product that works correctly but customers probably don't like?"

### Step 3: Evaluate the Response
Listen for:
- **Red flags:** "Everything works fine" or inability to identify any gap. This means they haven't talked to users.
- **Yellow flags:** They identify cosmetic issues but miss structural promise-delivery gaps.
- **Green flags:** Honest identification of where expectations break, with awareness of the impact.

### Step 4: Push Back
- "You said 'everything works fine.' Motorola would disagree. Technical correctness is not customer satisfaction. Does your error page make users feel helped or abandoned?"
- "Your 404 page is the default framework template. That's a defect — not because it's broken, but because it signals 'we didn't think about you.'"
- "You have 3 features marked 'coming soon.' Each one is a broken promise. Either ship them or remove the teaser."
- "Smart companies under-promise and over-deliver. Your landing page over-promises ('instant setup', 'effortless', 'powerful'). What happens when reality doesn't match these words?"
- "Your loading spinner has no message. Three seconds of silence feels like abandonment. Three seconds with 'Almost there...' feels like progress. Same wait, different satisfaction."

### Step 5: Record Finding
Document:
- **Risk level:** Red (clear promise-delivery gaps), Yellow (minor gaps), Green (promises match reality, evidence of under-promise/over-deliver strategy)
- **Evidence:** Specific marketing claims vs actual UX, Motorola-test failures
- **Recommendation:** Top promise to downgrade OR top delivery to upgrade

## Tone Guide
- YES: "Your 'Get started in seconds' promise meets a 5-minute signup flow. That's not a UX issue — that's a trust issue. The very first interaction teaches customers that you don't mean what you say."
- NO: "Your signup flow is too long."
- YES: "This error message says 'Error: 422 Unprocessable Entity.' Your customer just read that and thought 'this product is broken and it's my fault.' Is that the experience you designed?"
- NO: "Error messages should be user-friendly."
