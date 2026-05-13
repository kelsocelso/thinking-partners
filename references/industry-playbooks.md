# Industry Playbooks

Domain-specific lenses, gotchas, and signature moves. **Read the section matching the user's domain.** If you're not sure which domain the user is in, ask one clarifying question before going deep.

Sections in this file:
1. Consumer Apps, Mobile, Social, Games
2. Enterprise SaaS, B2B Infrastructure
3. AI / Deep Tech
4. Biotech, Life Sciences, Healthcare
5. Hardware, Robotics, Industrial
6. Fintech, Payments
7. Marketplaces
8. E-commerce, DTC, Retail
9. Hospitality, Experiences, Place
10. Creator Economy, Media, Content
11. Climate, Energy, Hard Tech
12. Education
13. Cross-domain patterns

---

## 1. Consumer Apps, Mobile, Social, Games

**Core voices:** Bier, Chesky, Wei, Sivers, Miyamoto, Meier, Wright, Newell, Norman, plus Bezos/Christensen on JTBD.

### What matters
- **First 60 seconds (Bier, Miyamoto).** Onboarding completion is the #1 fixable problem in most consumer apps.
- **The screenshot is the product (Bier).** App Store screenshots, share assets, friend's-phone moments.
- **Status engine (Wei).** What identity does using your product perform? Even non-social products have status implications.
- **Decision design (Meier).** Every meaningful choice in the product should be non-obvious, non-random, with consequence.
- **Happiness per dollar (Newell).** Monetization that respects the user wins long-term trust.
- **Retention by time horizon:** D1 = satisfying first session; D7 = habit/variety; D30 = identity/investment.

### Common failure modes
- "Better UX" without a moat.
- Beautiful product, no growth loop.
- Founder-only love (sample size of 1).
- Optimizing for screen-time instead of value (anti-Newell).
- Building features when onboarding is the actual problem.

### Monetization patterns
- **Free + ads:** screen-time max, often anti-player.
- **Paid one-time:** strong alignment, weak growth.
- **F2P + IAP:** can be aligned (cosmetics, convenience) or extractive (pay-to-win).
- **Subscription:** aligned with ongoing value, hard to convert.

### Distribution leverage points
- App Store search (own a keyword).
- ASA brand defense and broader keyword bidding (when retention metrics support it).
- Content-led (Reddit, TikTok, YouTube, Twitter) — pick the platform that matches the user.
- Viral primitives (share-your-result, invite mechanics).

---

## 2. Enterprise SaaS, B2B Infrastructure

**Core voices:** Levie, Slootman, Benioff, Rabois, Sacks, Elad Gil, Bret Taylor, Patrick Collison, Gurley, Dunford.

### What matters
- **JTBD clarity (Christensen).** B2B buyers buy when a job is painful enough; vitamins don't sell, painkillers do.
- **Three-buyer dynamic.** Buyer (signs check) ≠ champion (drives internally) ≠ user (operates daily). Sell to all three.
- **Switching costs as primary moat.** Depth of integration > breadth of features.
- **Cadence (Sacks).** Operating rhythm prevents drift. Weekly metrics, monthly funnel, quarterly strategy.
- **Execution culture (Slootman).** "Amp it up" — raise the bar, narrow focus, eliminate mediocrity.
- **AI transition (Levie).** Every B2B product needs to think about agent-first workflows in 2026.

### GTM motion selection
- **PLG:** low ACV, self-serve, single-user-decides.
- **Hybrid PLG+sales:** mid ACV, multi-user, no procurement.
- **Sales-led:** high ACV, multi-stakeholder, procurement.

### Common failure modes
- Building for "everyone" (kills positioning).
- Wrong motion (PLG product sold sales-led, or vice versa).
- Death by 1000 features instead of 10x on the one job.
- Wholesale "AI-washing" — adding LLM features that don't change core workflow.

### Pricing patterns
- Per-seat (declining in agent era).
- Consumption / volume.
- Per-outcome (newer, harder, more aligned).
- Enterprise tiers + custom pricing for scale.

---

## 3. AI / Deep Tech

**Core voices:** Hassabis, Amodei, Karpathy, Sutskever, Suleyman, Altman, Andreessen, Huang.

### What matters
- **Research bet vs. product bet.** Are you betting on capabilities emerging (research) or on packaging existing capability into a workflow (product)? Different funding needs, different timelines.
- **Scaling laws conviction.** Do you believe scale solves your problem, or do you need algorithmic breakthroughs?
- **Compute as cornered resource.** Compute commitments, GPU access, infrastructure deals.
- **Talent as cornered resource.** Research talent is concentrated; access is competitive.
- **Safety and alignment.** Responsible scaling, deployment risk, capability emergence.
- **Wrapper-vs.-native debate.** Are you building on top of foundation models (potentially commoditized as models improve) or building a model-native product?

### Common failure modes
- Wrapper products with no moat (next model generation makes them obsolete).
- Research without product path (no funding strategy).
- Product without research bench (no defense against better models).
- Underestimating distribution — model quality matters less than integration into existing workflows.

### Distribution patterns
- Existing platform integration (App Store, Chrome, IDEs, ChatGPT GPT Store).
- API/developer-first (Stripe-style — Anthropic's approach).
- Vertical workflow tools (Sierra-style — Bret Taylor's approach).
- Direct consumer (ChatGPT model, very few succeed).

---

## 4. Biotech, Life Sciences, Healthcare

**Core voices:** Afeyan, Church, Langer, Doudna, Swanson, Koller, Gawande, Murthy, plus Porter (industry structure) and Taleb (fat-tail exposure).

### What matters
- **Platform vs. product.** Platform companies (Moderna, Ginkgo, BridgeBio) generate multiple programs. Product companies bet on one drug. Different capital needs, different risk profiles.
- **Patient population definition.** Rare disease (small market, simpler trials, pricing power) vs. common disease (large market, complex trials, payer pressure).
- **Regulatory pathway clarity.** FDA fast-track? Breakthrough designation? Orphan drug? Path to approval matters as much as biology.
- **Three customers.** Patient (outcome) + prescriber (clinical use) + payer (reimbursement). Different incentives.
- **Founder pattern.** Scientist + operator pairing (Swanson/Boyer original; still relevant). Or scientist-CEO (newer, founder-led trend).
- **Capital strategy.** Biotech is fat-tailed — most programs fail, the few that succeed return the fund. Portfolio approach (Flagship, Third Rock) is antifragile. Single-program companies are fragile.

### Common failure modes
- Cool science, no clinical hypothesis ("we'll find a use for our platform").
- Underestimating regulatory timeline and cost.
- Building for the patient when the payer is the actual customer.
- Indication expansion without biological basis (Lens 1: Market trap).
- Underestimating manufacturing complexity (Process Power matters).

### AI + biology specifically (Koller / insitro pattern)
- Where does ML genuinely add edge? Usually: large dataset, repeated decisions, pattern recognition humans can't do at scale.
- Where does it add noise? Anywhere mechanistic biology is uncertain or training data is sparse.
- The data moat is real, but only if the data is proprietary AND structured AND large.

---

## 5. Hardware, Robotics, Industrial

**Core voices:** Musk, Fadell, Luckey, Straubel, plus Taleb (capital-intensive fat tails) and Helmer (Process Power, Scale Economies).

### What matters
- **Unit economics at scale (not at prototype).** First-unit cost ≠ thousandth-unit cost. Plan the cost-down curve.
- **Supply chain as moat.** Who controls components? Where's the concentration? Long-lead-time inputs (custom silicon, specialty materials) are leverage points.
- **Manufacturing learning curve (Process Power).** Hardware companies that don't internalize manufacturing learning lose.
- **First-principles thinking (Musk).** "What can you delete?" "The best part is no part."
- **Industrial design + soul (Fadell).** Hardware that's just functional loses to hardware that's also beautiful.
- **Speed of iteration (Luckey).** Anduril's edge is shipping defense hardware on tech-startup timelines.

### Common failure modes
- Designing for the demo, not the volume.
- Underestimating manufacturing complexity (the gap from prototype to product is massive).
- Single-supplier dependency (one component blows up, you're dead).
- Software-style monthly releases applied to hardware (impossible).
- Forgetting industrial design (the unboxing moment matters).

### Distribution patterns
- Pre-orders + waitlist + community.
- Crowdfunding for validation (not just capital).
- Retail channel (still important for consumer hardware).
- Direct-to-consumer + tier-1 enterprise pilots.

---

## 6. Fintech, Payments

**Core voices:** Collison brothers, Levchin, Tenev, Vélez, Schulman, plus Gurley (unit economics), Munger (risk), Porter (regulated-industry structure).

### What matters
- **Regulatory licenses as Cornered Resource.** Money transmitter licenses, banking partnerships, payment processor relationships — slow, valuable, defensible.
- **Underwriting / risk-pricing edge.** ML-driven underwriting can be real moat (Affirm pattern) or marketing veneer over adverse selection.
- **Switching costs.** Where money flows is sticky — but not impossibly sticky. Wallet position matters.
- **Trust as brand asset (Vélez).** In regulated industries, trust is a moat. Building it is slow.
- **Compliance as feature, not afterthought.** Built-in compliance is a competitive advantage; bolted-on is liability.

### Common failure modes
- CAC-buying volume without underwriting edge (negative unit economics).
- Underestimating regulatory cost and timeline.
- Gamification at the cost of trust (Robinhood backlash).
- "We'll figure out the bank partnership later" (often catastrophic).

### Distribution patterns
- Embedded finance (B2B2C — banking-as-a-service into vertical apps).
- Direct consumer with viral mechanics (Venmo, Cash App).
- B2B sales-led (corporate cards: Brex, Ramp).
- Crypto-native distribution (different regulatory regime, different mechanics).

---

## 7. Marketplaces

**Core voices:** Gurley, Chen (cold start), LaFontaine, Chesky (Airbnb pattern).

### What matters
- **Solve the chicken-and-egg first.** Subsidize one side until liquidity tips. (Gurley playbook.)
- **Identify which side is harder to acquire.** Build for them.
- **Take-rate ceiling.** Some categories support high take-rate (Airbnb 15%+), others can only sustain 5%. Know yours.
- **Liquidity > selection** in early days. A small, dense marketplace > a large, sparse one.
- **Disintermediation risk.** Can buyers and sellers transact off-platform after meeting? Lower if you provide payment, trust, dispute resolution.

### Common failure modes
- Trying to grow both sides at once (usually means neither tips).
- Choosing the wrong side to subsidize.
- Tolerating disintermediation (death by a thousand off-platform deals).
- Take-rate too high too fast (sellers defect).

---

## 8. E-commerce, DTC, Retail

**Core voices:** Drexler, Chouinard, Blakely, Weiss, Lake, Amoruso, Andy Dunn, Lütke, plus Gurley on unit economics.

### What matters
- **Brand-as-moat.** In a commodity-saturated world, brand is one of the few sustainable advantages for physical goods.
- **Vertical vs. wholesale.** "Digitally-native vertical brand" (Dunn) means controlling the customer relationship end-to-end.
- **CAC payback.** DTC unit economics are brutal. If LTV/CAC ratio isn't strong by year 1, you're in trouble.
- **Retention drives the model.** Subscription, replenishment, or strong repeat-purchase categories work; one-time-purchase categories struggle.
- **Inventory risk.** Cash tied up in inventory kills DTC startups.

### Common failure modes
- Confusing GMV growth with profitable growth.
- Acquiring customers at unsustainable CAC, expecting LTV that doesn't materialize.
- Brand voice that's inconsistent across touchpoints.
- Going too broad too fast (Allbirds beyond shoes, e.g.).

### Distribution patterns
- Founder-led brand (Hewitt, Amoruso pattern).
- Influencer + creator partnerships.
- Retail channel partnerships (still relevant — Target, Sephora, etc.).
- Owned content (Glossier blog → product).

---

## 9. Hospitality, Experiences, Place

**Core voices:** Meyer, Chesky, Branson, Wilson, plus Norman on experience design.

### What matters
- **Enlightened hospitality (Meyer).** Staff first, then guests. Culture is the product.
- **The 11-star experience (Chesky).** What does the *insane* version look like? The gap between 5-star and 11-star is where the brand lives.
- **Community-driven category creation (Wilson, Lululemon).** Ambassadors, identity-signaling.
- **Brand portfolio (Branson).** Does the brand stretch across categories without breaking?
- **Operational excellence + emotional moments.** Both required; one alone isn't enough.

### Common failure modes
- Service excellence without hospitality (technically correct, emotionally cold).
- Brand expansion that dilutes (every category exposes the brand to failure).
- Underestimating local/cultural adaptation.

---

## 10. Creator Economy, Media, Content

**Core voices:** Ben Thompson, Casey Newton, Mr. Beast, Joe Pulizzi, Bari Weiss, Hewitt, plus Wei on status dynamics.

### What matters
- **Audience-first (Pulizzi).** Build audience before product. The audience is the moat.
- **Creator-as-channel.** The founder/creator IS the distribution.
- **Aggregation Theory (Thompson).** Who controls demand — supplier, platform, or user? Strategy follows.
- **Thumbnail / hook discipline (Mr. Beast).** Content quality matters less than retention curve discipline.
- **Editorial POV.** What's the strong opinion that displaces generic alternatives?

### Common failure modes
- Product-first (then trying to "find audience").
- Diversifying revenue before audience is durable.
- Diluting the voice for broader appeal (loses the core fans).
- Underestimating production cost as you scale.

### Distribution patterns
- Owned channel (newsletter, podcast, YouTube) → audience → monetization.
- Platform-dependent (TikTok, YouTube, Twitter) — fast growth, fragile.
- Subscription (Substack, Patreon, paid newsletter).
- Sponsorship + product extension.

---

## 11. Climate, Energy, Hard Tech

**Core voices:** Griffith, Doerr, Khosla, Straubel, plus Musk on first principles.

### What matters
- **Deployment problem, not invention problem (Griffith).** Most climate tech already exists. The bottleneck is rolling it out.
- **Speed and scale (Doerr).** Gigaton-level impact requires both.
- **Policy environment.** Subsidies, mandates, procurement schedules drive everything.
- **Cost-down curves.** Solar, batteries, etc. follow learning curves. Position for the curve.
- **Procurement as customer.** Government, utilities, large corporates are early customers — slow but durable.

### Common failure modes
- Cool tech that can't deploy at scale (impressive demo, no rollout plan).
- Underestimating policy and procurement timelines.
- Ignoring the installer/operator/maintenance layer (deployment is execution).
- Single-policy-regime dependency (one election can change the picture).

---

## 12. Education

**Core voices:** Khan, Koller, Agarwal, Thrun.

### What matters
- **Mission compatibility with business model.** Mission-led free distribution (Khan Academy) vs. premium learning (Coursera Plus) — both work, but they're different businesses.
- **Career outcome as metric.** Not course completion. Be honest about whether the learner gets the job/skill/raise.
- **Credentialing matters.** Is your credential recognized, transferable, durable?
- **AI tutoring shift.** Khanmigo-style AI tutors are changing the unit economics of personalization.

### Common failure modes
- Course completion as success metric (vanity).
- Building for B2C when B2B (enterprise, university partnership) is the better model — or vice versa.
- Underestimating regulatory and accreditation requirements.

---

## 13. Cross-domain patterns

Some patterns transfer across all the above:

### "What would have to be true" (Noubar Afeyan via biotech, applies everywhere)
Instead of arguing for an idea, ask: "What would have to be true for this to be a great business?" Then test each premise. Surfaces the riskiest assumption.

### Working backwards (Bezos)
Write the press release / launch announcement / customer testimonial before building. If it's boring, the product idea is probably boring.

### Inversion (Munger)
"How does this fail?" applied to every assumption surfaces hidden risks faster than positive analysis.

### Barbell strategy (Taleb)
Most resources on safe positions. Small allocation on asymmetric upside bets. Medium-risk is where capital goes to die.

### First principles (Musk)
Reason from atoms, not from analogies. What's the physics/biology/economics-level constraint?

### Compounding (Lütke, Huang, Buffett)
What activity, repeated weekly, compounds toward a Power? Most of company-building is showing up for that activity for years.

---

## Notes for the assistant

- **Read only the section matching the user's domain.** Don't load the whole file as context.
- **Cross-pollinate cautiously.** A pattern from biotech (portfolio approach to fat-tailed bets) might apply to early-stage consumer apps. But don't force frameworks across domains.
- **If the user is in a domain not listed here, ask one clarifying question and synthesize from related domains.**
- **The user's existing business may shift the lens.** A solo indie founder needs different framing than a Series C operator. Stage matters as much as industry.
