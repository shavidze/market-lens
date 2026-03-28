# Market Lens — Frameworks Knowledge Base

This document contains the theoretical foundation for all 4 lenses, derived from Kotler's Principles of Marketing. Use these frameworks to ground your analysis — but always translate theory into specific, actionable findings tied to what you observe in the codebase.

---

## Lens 1: Myopia Check

### Core Principle
Marketing myopia occurs when sellers focus on the product rather than the underlying need it satisfies. "The drill manufacturer may think the customer needs a drill, but what the customer really needs is a hole."

### Key Concepts
- **Needs** are basic human states of deprivation (food, shelter, belonging, self-expression). They are NOT invented by marketers — they are fundamental.
- **Wants** are the form needs take when shaped by culture and individual personality. A hungry person in Bahrain wants vegetable curry; in Eindhoven, a ham-and-cheese roll.
- **Demands** are wants backed by purchasing power. Honda Civic = basic transport + low price. Mercedes = comfort + luxury + status.
- **Marketing myopia** = obsession with the product, blindness to the underlying need. Railroad managers thought customers wanted trains, not transportation — and missed the rise of airlines, buses, and cars.

### What to Look For in Code
- README/docs that describe features without explaining the problem being solved
- Navigation and menus structured around product capabilities instead of user goals
- Feature naming that uses internal/technical jargon instead of customer language
- Landing page copy that leads with "what we built" instead of "what you need"
- Absence of user-centric language ("you", "your problem", "your goal")

### The Draker Test
> "The aim of marketing is to make selling superfluous. The aim is to know and understand the customer so well that the product or service fits them and sells itself." — Peter Drucker

If you can't describe the product without mentioning a single feature, you have myopia.

---

## Lens 2: Value Perception

### Core Principle
Customer value is the difference between the benefits a customer gains from owning/using a product and the costs of obtaining it. Customers act on **perceived value**, not objective value.

### Key Concepts
- **Benefits:** functional (it works), emotional (it feels good), social (status/image), convenience (saves time/effort)
- **Costs:** monetary (price), time (learning curve, setup), effort (complexity), psychological (risk, anxiety, decision fatigue)
- **Perceived value** drives decisions — Federal Express customers pay more because they *perceive* faster, more reliable delivery, plus status ("using FedEx makes sender and receiver feel more important")
- Customers compare value across alternatives: FedEx vs UPS vs DHL vs postal service
- Products are seen as **bundles of benefits** — customers choose the bundle that delivers the most satisfaction for their money

### What to Look For in Code
- Pricing page: Is value clearly communicated? Or just feature lists?
- Onboarding flow: How much effort/time before the user gets value? (time-to-value)
- Signup friction: How many steps? What information is demanded upfront?
- Free vs paid boundaries: Does the free tier demonstrate enough value to convert?
- Cost signals: Hidden costs (forced logins, mandatory emails, complex setup)
- Value communication: Does the UI surface benefits or just functionalities?

### The FedEx Test
For each feature/page, ask: "What benefit does the customer *perceive* they're getting, and what are they *perceiving* they're paying (money, time, effort, anxiety)?"

---

## Lens 3: Satisfaction Risk

### Core Principle
Customer satisfaction depends on the product's perceived performance relative to the buyer's expectations.
- Performance < Expectations → **Dissatisfied**
- Performance = Expectations → **Satisfied**
- Performance > Expectations → **Delighted**

Smart companies aim for delight: promise only what you can deliver, then deliver more than promised.

### Key Concepts
- **Quality = customer satisfaction**, not "absence of defects"
- **Motorola's definition:** "If the customer doesn't like it, it's a defect" — regardless of whether it's technically correct
- **TQM (Total Quality Management):** Quality starts with customer needs and ends with customer satisfaction
- **The promise-delivery gap:** Marketing copy sets expectations. The actual product experience delivers (or fails to deliver) on them.
- **Under-promise, over-deliver:** The winning strategy. If you promise X and deliver X+1, the customer is delighted. If you promise X+2 and deliver X+1, the customer is disappointed — even though the outcome is the same.

### What to Look For in Code
- Marketing copy vs actual UI: Does the landing page promise things the product doesn't fully deliver?
- Error messages: Are they helpful and human, or cryptic and blaming?
- Loading states: Does the UI feel responsive, or does it leave users hanging?
- Empty states: When there's no data, does the product guide users, or show a blank void?
- Edge cases: How does the product behave when things go wrong?
- Feature completeness: Are there half-built features visible to users?
- Onboarding promises vs reality: Does the first-run experience match what was advertised?

### The Motorola Test
Walk through the product as a first-time user. Every moment of confusion, friction, or disappointment is a "defect" — regardless of whether the code works correctly.

---

## Lens 4: Retention Signal

### Core Principle
Acquiring a new customer costs **5x more** than retaining an existing one. Losing a customer means losing their entire lifetime stream of purchases — a Ford customer's lifetime value can exceed £250,000.

### Key Concepts
- **Transaction marketing** focuses on individual sales. **Relationship marketing** focuses on long-term relationships.
- **Marketing networks:** Company + all supporting stakeholders (customers, employees, suppliers, distributors). Competition increasingly happens between networks, not companies.
- **The leaky bucket:** Growing markets let you ignore retention. Stagnant/shrinking markets punish companies that don't retain.
- **Customer lifetime value (CLV):** One transaction is the tip of the iceberg. The real value is the full relationship over time.
- **Principle:** "Build a good network of relationships with key stakeholders, and profits will follow."

### What to Look For in Code
- Returning user flows: Is there a differentiated experience for returning users?
- Engagement hooks: Email notifications, progress tracking, streaks, reminders
- User data persistence: Does the product remember user preferences/history?
- Communication channels: Email templates, notification systems, in-app messaging
- Community features: Comments, sharing, collaboration, social proof
- Feedback mechanisms: Rating systems, surveys, feedback forms, support channels
- Churn signals: Are there any anti-churn mechanisms (win-back emails, re-engagement)?
- Absence of retention patterns: If none of the above exist, the product is built for one-time use

### The Relationship Test
Ask: "After the first use, what reason does the user have to come back tomorrow?" If the answer is "none" — that's the biggest finding.
