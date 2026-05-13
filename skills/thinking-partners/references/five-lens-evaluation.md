# The 5-Lens Evaluation

The default playbook for Evaluate Mode. Use when the user asks "what do you think of this", "is this any good", "should I build this", or wants a structured assessment.

Goal: produce an honest verdict in ~5–10 minutes of thinking, not a 30-page report. Be specific to the user's actual product, industry, and situation. **Discovery before verdict** — never rate on partial data.

---

## How to run it

The flow is **Discovery → Score → Verdict.** Don't skip discovery to get to the verdict faster.

1. **Detect the domain.** Is this consumer app, enterprise SaaS, biotech, hardware, fintech, marketplace, creator economy, climate, AI/deep tech, education, retail/DTC, hospitality? The lenses adapt to the domain.
2. **Restate what you're evaluating in one sentence.** Force precision. If you can't restate cleanly, ask one clarifying question first.
3. **Offer the path.** "Full discovery (5–10 min of questions, real verdict) or quick directional read (low-confidence, based on what you've already said)?" Honor the choice.
4. **Run the Discovery flow** (next section) until the minimum data gate is filled.
5. **Score each lens** 🟢 strong / 🟡 mixed / 🔴 weak — with one specific reason each.
6. **Render the recommendation** (🟢 Green / 🟡 Yellow / 🔴 Red) in the format below.

---

## Discovery: questions before verdict

**Principle:** the verdict is only as good as the data behind it. Ask before you assess. Use the AskUserQuestion tool (when available) for closed/structured items — give 4 options plus an "Other" escape hatch. Use open-ended prompts for the things the user needs to articulate in their own words (wedge, moat thesis, why-now). Always explain the concept in one line *before* asking — most users haven't internalized these definitions.

**Be progressive, not a survey.** Ask 2–4 questions per round. React to the answers. Pull threads. Don't dump all 15 questions at once.

### Context questions (load first — they shape everything)

**Stage** *(use AskUserQuestion)*
"Where are you in the build?"
- Pre-idea (still deciding what to work on)
- Idea, not built
- Building, pre-launch
- Launched, pre-PMF
- Launched with traction
- Scaling

**Business model** *(use AskUserQuestion)*
"How does this make money?"
- Subscription
- Transactional / per-use
- Marketplace fee
- Ads
- Hardware sale
- Services / consulting
- Other (describe)

**Target customer** *(open-ended — force specificity)*
"Who's the customer? Be specific — 'busy moms 30–45 using fitness apps' beats 'health-conscious people.' If the answer is 'everyone,' the wedge isn't real yet."

**Investment so far** *(use AskUserQuestion)*
"How much have you put into this?"
- Just time, no money
- Under $10k
- $10k–$100k
- $100k–$1M
- $1M+

### Market questions

**Explain first:** "A real market means there are buyers who could plausibly write you a check today — not a TAM slide, a credible bottom-up wedge that compounds."

- *Open:* "Who are your beachhead 100 customers — the first set you can name or describe by archetype?"
- *Open:* "How are they solving this problem today? What do they pay for currently?"
- *AskUserQuestion — Why now:* "What changed in the last 18 months that makes this winnable now?"
  - Tech unlock (LLMs, new API, new platform)
  - Behavior shift (post-COVID, remote, demographic)
  - Regulation (new law / deregulation)
  - Cost curve (something got cheap)
  - Incumbent failure (someone left a gap)
  - Honestly, nothing specific changed

### Moat questions

**Explain first:** "A moat is a durable competitive advantage that strengthens with scale. Not a feature. Not better UX. Hamilton Helmer's 7 Powers is the canonical list of what actually counts as one."

- *AskUserQuestion — Map to a Power:* "Which of the 7 Powers is your moat thesis?"
  - Scale Economies (cost per unit drops with size)
  - Network Economies (product gets better as more users join)
  - Switching Costs (users pay a cost to leave)
  - Branding (durable trust premium)
  - Cornered Resource (exclusive access — IP, supply, contract)
  - Counter-Positioning (incumbents structurally can't follow)
  - Process Power (operational know-how compounds over time)
  - None yet — competing on execution
- *Open:* "Describe your moat in one sentence. What's the durable thing?"
- *Open:* "If a well-funded competitor copies your product feature-for-feature next quarter, what survives?"
- *Open:* "What gets stronger as you scale?"

### Product / Wedge questions

**Explain first:** "A wedge is the narrow entry point where you win — a specific user, doing a specific job, that no one else does well today. The wedge is what gets you to 1,000 customers. The market is what gets you to 100,000."

- *Open:* "Describe your wedge in one sentence: who, doing what, that no one else does well today?"
- *AskUserQuestion — Painkiller or vitamin:* "Is this a painkiller or a vitamin for the customer?"
  - Painkiller — they have an acute, named problem they're actively trying to solve
  - Vitamin — it's a nice-to-have, would-be-good-to-fix
  - Honestly unsure
- *Open:* "What's the 10× claim? What makes this 10× better than the current alternative for this specific user?"

### Distribution questions

**Explain first:** "Distribution is how the first 1,000 — then 100,000 — customers actually find and adopt this. Brian Balfour's frame: market + product + channel + model must all fit together. A great product in the wrong channel dies."

- *AskUserQuestion — Primary channel:* "What's your primary acquisition channel?"
  - Organic search / SEO
  - Paid acquisition (ads)
  - Viral / referral loops
  - Sales-led (outbound, demos)
  - Community / content
  - Partnerships / integrations
  - Press / influencer
  - I don't know yet
- *Open* (if launched): "Have you tested it? What's your rough CAC vs. LTV?"
- *Open:* "Is your channel saturated or favoring incumbents? Why is it open for you?"

### Customer / Retention questions

**Explain first:** "Pre-launch, 'customer' is a theory about who will love this. Post-launch, it's the most honest signal you have — retention and word-of-mouth beat every other lens combined."

- *AskUserQuestion — PMF signal:* "Where are you on retention / PMF signal?"
  - Not launched yet
  - Launched, no retention data yet
  - Have data, retention is weak
  - Have data, retention is solid
  - Have data, retention is exceptional (users telling friends unprompted)
- *Open:* "Smallest viable audience: who are the 100 people who'd be devastated if this disappeared tomorrow? Do they exist? Can you reach them?"
- *Open* (if launched): "What are users telling you in their own words right now — quotes if you have them?"

---

## Minimum data gate

**Do not render a recommendation until you have:**
1. **Stage** (closed)
2. **Business model** (closed)
3. **Specific target customer** (not "everyone")
4. **User's own wedge description** (one sentence, in their words)
5. **User's own moat thesis** — mapped to a Power, or an honest "none yet, competing on execution"
6. **One current-state datapoint** OR explicit acknowledgment of "this is pre-data theory"

If any are missing, say what's missing and offer to walk through it:
> "I'd be guessing without [stage / wedge description / moat thesis / retention signal]. Want to walk through those, or do you want a low-confidence directional read?"

A confident-sounding verdict on five hand-waved lenses is worse than no verdict.

---

## Lens 1: Market

*Default voices: Rachleff, Andreessen, Thiel.*

**Core question:** Is the market real, big enough, growing, underserved?

**Sub-prompts by domain:**
- **Consumer:** Who specifically is the customer? Is the market growing? Is the underlying behavior (gaming, dating, fitness) expanding or contracting? Where's the wave (platform shift, demographic shift, cultural shift)?
- **Enterprise SaaS:** What budget does this come out of, and is that budget growing? Who's the buyer vs. the user? Is this a "must-have" or a "nice-to-have" in a 2026-budget review?
- **Biotech:** What's the patient population? Is there an unmet medical need (Christensen JTBD applied to disease)? Is the regulatory path clear? Who pays — insurance, patient, government?
- **Hardware:** What's the unit economics at scale (not at prototype)? Is the cost-down curve real?
- **Fintech:** What regulatory regime are you operating in? Is there a defensible underwriting edge, or are you just CAC-buying volume?
- **Marketplace:** Is supply or demand the constraint? What's the take-rate ceiling?
- **Climate / hard tech:** What's the deployment curve, not the invention curve? Is the policy environment favorable or hostile?
- **AI / deep tech:** Is this a research bet or a product bet? Is the underlying capability mature, or are you betting on emergence?

**Watch for:**
- TAM hand-waving without a credible bottom-up wedge.
- "The market should exist" (often means no one actually wants this).
- Counter-positioning opportunity (incumbents structurally can't follow you).

---

## Lens 2: Moat

*Default voices: Helmer, Thiel, Porter. Add Taleb for fat-tail/asymmetry framing.*

**Core question:** Which of the 7 Powers could this earn, or is this competing on execution alone?

**Sub-prompts:**
- Run through the 7 Powers: Scale Economies, Network Economies, Counter-Positioning, Switching Costs, Branding, Cornered Resource, Process Power. Which one(s) are credible — *with both benefit and barrier*?
- If "none yet" — is there a path to one? What has to happen first?
- Thiel test: if a well-funded competitor copied this tomorrow, what stops them?

**Domain-specific moat patterns:**
- **Consumer mobile:** Most credible early Powers are Branding and Switching Costs (data, progress, social graph). Network effects are weak in solo experiences, strong in social.
- **Enterprise SaaS:** Switching Costs (deep integrations, data lock-in), Scale Economies (R&D amortization), Branding (Salesforce-tier trust).
- **Biotech:** Cornered Resource (IP, specific compound), Process Power (manufacturing know-how, regulatory experience), Branding (clinician trust).
- **Hardware:** Scale Economies (per-unit cost curve), Process Power (manufacturing learning curve), Cornered Resource (supply chain access).
- **Marketplace:** Network Economies (canonical), supply density as switching cost for buyers.
- **Fintech / payments:** Switching Costs (where money flows already), Scale Economies (risk underwriting improves with volume), regulatory licenses as Cornered Resource.
- **Creator economy:** Branding (founder/creator IP), Switching Costs only if you accumulate something irreplaceable.

**Watch for:**
- "First mover advantage" claimed as a moat. (It's not.)
- "Better UX" claimed as a moat. (It's not, unless paired with switching costs or brand.)
- Brand claimed as a moat for a product with no loyalty signal yet.

---

## Lens 3: Product

*Default voices: Jobs, Chesky, Christensen, Norman.*

**Core question:** What job is the customer hiring this for, and is the product 10x better at that job?

**Sub-prompts:**
- JTBD: what progress is the customer trying to make? What were they doing before? What are they firing to hire you?
- Vitamin or painkiller? (Painkillers fund themselves; vitamins need marketing.)
- Chesky's 11-star test: what would the *insane* version look like? Where on 1–11 are you?
- Norman's usability check: where's the friction the user shouldn't be experiencing?

**Domain-specific notes:**
- **Consumer:** Emotional response matters as much as functional outcome. Does the user *feel* something?
- **Enterprise:** Functional outcome dominates; emotion is secondary. Does this save time or money in a way the buyer can defend?
- **Biotech:** "Product" is a therapy — efficacy, safety, route of administration, dosing. Is it differentiated on a dimension that matters clinically?
- **Hardware:** Industrial design + functional excellence. Does it have a soul (Fadell test)?
- **AI/deep tech:** Is the capability actually there, or are you wrapping marginal capability in product polish?

**Watch for:**
- Feature lists masquerading as product strategy.
- "10% better" in markets that demand 10x better.
- Products that work but don't make anyone *feel* anything.

---

## Lens 4: Distribution

*Default voices: Bier (consumer), Dunford (positioning), Chen/Balfour (loops), Sacks (B2B GTM), Raskin (narrative).*

**Core question:** How does the next user find this, and is the channel structurally aligned with the product and model?

**Sub-prompts:**
- What's the growth *loop*, not the funnel? How does one user produce the next?
- Four Fits (Balfour): product/channel/model/market alignment.
- Dunford positioning: what one sentence makes a stranger get it? What are they comparing it to?

**Domain-specific distribution patterns:**
- **Consumer mobile:** App Store search/ASA, viral loops, content marketing, influencer. Bier-style hook + screenshot strategy.
- **Enterprise SaaS:** PLG (Tope Awotona — product is the distribution), inbound content (Benioff playbook), outbound sales (David Sacks's cadence), partnerships.
- **Biotech:** KOL (key opinion leader) engagement, clinical trial visibility, pharma BD partnerships, regulatory pathway clarity.
- **Hardware:** Pre-order + waitlist + early-adopter community → retail channel. Crowdfunding for validation.
- **Marketplace:** Solve the chicken-and-egg first — pick one side to subsidize (Gurley playbook).
- **Climate / hard tech:** Policy and procurement matter more than marketing. Who's the first government or utility customer?
- **AI products:** Distribution often through existing platforms (App Store, Chrome, ChatGPT GPT Store). Native AI workflow apps need different motion.
- **Creator economy:** The creator *is* the distribution. Audience-build precedes monetization.

**Watch for:**
- Products with no native distribution mechanism that the founder plans to "market into" — rarely works without large budgets.
- Channel/product mismatch (viral consumer mechanics on a slow enterprise sale, or vice versa).
- Treating "we'll figure out marketing later" as a strategy.

---

## Lens 5: Customer

*Default voices: Bezos, LaFontaine, Weiss, Godin (smallest viable audience).*

**Core question:** Who specifically would love this enough to tell a friend?

**Sub-prompts:**
- Name 3 specific people in this audience. Actual humans, not personas.
- Bezos working-backwards: write the press release. Is the headline interesting?
- Smallest viable audience: who's the group of 100 people who'd be *devastated* if this disappeared? Do they exist? Can you reach them?
- Is there a community already gathering around this need?

**Domain-specific notes:**
- **Consumer:** The smallest-viable-audience question is doing most of the work. Avoid "everyone could use this."
- **Enterprise:** The buyer ≠ the user ≠ the champion. Who's each? Are you serving the buyer's CYA needs or the user's actual workflow?
- **Biotech:** The patient is one stakeholder; the prescriber, the payer, and the regulator are others. Whose problem are you actually solving?
- **Marketplace:** Who's the side that's hardest to acquire? Build for them first.
- **Creator economy:** Are *you* the customer (in disguise as the founder), or are you serving someone whose needs you've actually validated?

**Watch for:**
- Generic personas ("women 25–45 who like X").
- Founder-only love ("I would use this" — that's a sample size of one).
- "Everyone could use this" — usually means no one specifically loves it.

---

## The Recommendation

Once the minimum data gate is filled and you've scored each lens, render the verdict in this exact shape. **Show your work first** — recap what the user told you so they can correct misreads before the call lands.

### Pre-verdict recap

> **Based on what you told me:**
> - Stage: [pre-PMF / launched / etc.]
> - Model: [subscription / transactional / etc.]
> - Customer: [specific archetype, in user's own words]
> - Wedge: [user's one-sentence wedge]
> - Moat thesis: [Power mapped to, or "none yet"]
> - Current data: [retention / revenue / "pre-data theory"]
>
> *If any of this is wrong, tell me and I'll re-score.*

### Lens scorecard

> - **Market** 🟢/🟡/🔴 — [one-sentence specific reason, citing user's context]
> - **Moat** 🟢/🟡/🔴 — [one-sentence specific reason]
> - **Product / Wedge** 🟢/🟡/🔴 — [one-sentence specific reason]
> - **Distribution** 🟢/🟡/🔴 — [one-sentence specific reason]
> - **Customer / Retention** 🟢/🟡/🔴 — [one-sentence specific reason]

### Recommendation

Pick one. State it firmly. No theatrics, no hedging.

#### 🟢 Green light — Build it. Scale it. Move with conviction.

> **🟢 Recommendation: Green light.**
>
> *Hitting:* [2–4 lenses where they're genuinely strong, named specifically — e.g. "durable moat via Switching Costs from workflow lock-in," "clear painkiller for a named ICP," "non-saturated channel that fits the model"]
>
> *Watch:* [1–2 areas that aren't dealbreakers but could become them]
>
> *Kill conditions* — what would invalidate this green light in the next 6 months: [1–3 specific events / metrics]
>
> *Confidence:* high / medium / low. [One line on what would raise it — usually code access, post-launch data, or a specific customer conversation]
>
> *Next move:* [the single highest-leverage thing to do this week or month]

#### 🟡 Yellow light — Proceed, but time-box and define the exit. Don't sink runway on this without a PMF signal.

> **🟡 Recommendation: Yellow light.**
>
> *Hitting:* [the lenses strong enough to justify continuing]
>
> *Missing or weak:* [the lenses that need to firm up]
>
> *The test* — the specific experiment that would move this to green: [concrete metric + deadline. e.g. "Share-rate >15% in 60 days," "10 named ICP customers willing to pay within 90 days," "Retention curve flattens above 20% by month 3"]
>
> *Pivot trigger* — what forces a pivot or kill if the test fails: [specific condition]
>
> *Confidence:* and what would change it.

#### 🔴 Red light — Don't build in current form. Specific reasons, not vibes.

> **🔴 Recommendation: Red light.**
>
> *Why* — the 1–3 structural problems that aren't fixable inside the current frame: [no real moat path / fundamentally crowded market with no wedge / channel doesn't fit model / vitamin not painkiller / something specific to their context]
>
> *What's salvageable:* [name the kernel if there's one worth keeping. If there isn't, say so — don't manufacture a pivot to soften the call]
>
> *Closest adjacent idea worth exploring:* [only if there's a real one — otherwise omit]
>
> *Confidence:* high reds need high confidence. State what evidence drove the call.

### Always end with one line

> *Want me to re-run this if [X] changes — post-launch data, a new channel test, or you sharpen the wedge?*

This turns the verdict into a working document, not a one-shot judgment.

---

## Stage-weighted scoring

Same five lenses, different weights by stage. Don't pretend a pre-launch idea and a $5M-ARR business are evaluated the same way.

- **Pre-idea / idea-stage:** Weight Market and Wedge heaviest. Moat is theoretical — fine to grade it on the *path* to a Power, not the current state. Distribution can be a hypothesis. Customer / Retention is theoretical.
- **Building, pre-launch:** Wedge and Distribution-fit matter most. Moat path should be clearer. Customer should be specific (named design partners, waitlist quality).
- **Launched, pre-PMF:** Customer / Retention becomes the dominant signal. Wedge can be re-evaluated against actual user behavior. Distribution: have you tested it, what's CAC?
- **Launched, with traction:** Moat (is the Power compounding?) and Distribution (does the channel scale, or is CAC climbing?) become the binding constraints.
- **Scaling:** Process Power, Brand, and unit economics dominate. Wedge is mostly historical.

---

---

## Worked examples

### Example 1: Consumer mobile

> **User:** "Should I add a social leaderboard to my puzzle game to drive retention?"

**Domain:** consumer mobile, casual game.
**Restated:** Adding asynchronous social comparison to a solo puzzle game to lift retention.

- **Market** 🟡 — Demand exists (NYT Games, Wordle daily-compare loop), but solo puzzle audiences skew non-social.
- **Moat** 🔴 — Leaderboards are a feature, not a moat. Add Switching Costs *only* if friends actually join (cold-start problem).
- **Product** 🟡 — Could be 10x for comparison-seekers, risks cluttering core solo experience.
- **Distribution** 🟢 — If implemented as viral loop (share scores), this is one of the few consumer-social mechanics available in puzzle. Real Bier-style hook potential.
- **Customer** 🔴 — Existing users haven't shown signal they want social. Retention problem might be upstream (onboarding) not downstream (social).

**Verdict:** 🟡 **Go with conditions.** Don't build leaderboards. Build a *share-your-score* primitive first — tests the underlying hypothesis at 10% of the cost. Only build full social if share-rate exceeds a threshold.

**Biggest single risk:** 4–6 weeks building social infrastructure that solves a retention problem actually shaped like onboarding.

### Example 2: Enterprise SaaS (full new format)

> **User:** "Should I build an AI agent for SOC analysts to triage alerts?"

**After discovery, you have:** Stage = idea, pre-build. Model = enterprise subscription. Customer = mid-market CISOs at companies with 50–500-person eng orgs. Wedge (user's words): "tier-1 alert triage for SOCs without dedicated AI engineers." Moat thesis: Switching Costs (agent learns the customer's environment) + Process Power over time. Data: zero — pre-launch theory.

**Based on what you told me:**
- Stage: idea, pre-build.
- Model: enterprise subscription.
- Customer: mid-market CISOs (50–500-person eng orgs).
- Wedge: tier-1 alert triage for SOCs that don't have dedicated AI engineers.
- Moat thesis: Switching Costs (env-specific tuning) + Process Power.
- Current data: pre-launch theory.

*If any of this is wrong, tell me and I'll re-score.*

**Lens scorecard:**
- **Market** 🟢 — Real budget (security ops), alert-volume growth is the painkiller; analyst burnout is a named, urgent problem.
- **Moat** 🟡 — Switching Costs and Process Power are theoretically credible but unproven; CrowdStrike/Palo Alto can ship "good enough" AI on existing platforms.
- **Product / Wedge** 🟢 — Painkiller for a named ICP. "Tier-1 triage" is narrow enough to win.
- **Distribution** 🔴 — Enterprise security sale is 6–12 months, multi-stakeholder, SOC2 required. Slowest GTM in the wedge.
- **Customer / Retention** 🟡 — Buyer (CISO) ≠ champion (SOC manager) ≠ user (analyst). Misalignment is the most common failure mode in this category.

**🟡 Recommendation: Yellow light.**

*Hitting:* clear painkiller, real budget, named ICP, defensible long-term moat path.

*Missing or weak:* no proof the moat compounds before incumbents bundle, no validated GTM in a slow enterprise cycle, no design partner.

*The test:* sign one named design-partner CISO who'll co-build on real alert data within 90 days, and ship a working triage agent against their alerts within 6 months that demonstrably reduces tier-1 analyst time by 30%+.

*Pivot trigger:* if no design partner closes in 90 days, or CrowdStrike/Palo Alto announces a comparable AI feature before you ship, kill or pivot to a vertical incumbents won't touch.

*Confidence:* medium. Would update with: actual conversations with 3+ CISOs, current incumbent product roadmaps, and code grounding once a prototype exists.

*Want me to re-run this if you land a design partner or a competitor moves?*

### Example 3: Biotech

> **User:** "Should we extend our oncology platform into autoimmune?"

**Domain:** biotech platform company, indication expansion.
**Restated:** Whether to extend an existing oncology drug-discovery platform into autoimmune disease indications.

- **Market** 🟢 — Autoimmune is a huge market (>$100B globally), with continued growth, multiple unmet needs across IBD, lupus, MS, etc.
- **Moat** 🟡 — Your Cornered Resource (the platform) might apply, but autoimmune biology is genuinely different — your tumor immunology insights may not transfer. Process Power doesn't carry over automatically.
- **Product** 🟡 — Is the platform mechanism actually relevant to autoimmune pathways? Need biology answer before strategy answer. Don't extend just because the market is bigger.
- **Distribution** 🟡 — Different KOLs, different pharma partners, different clinical infrastructure. You're starting over on relationships.
- **Customer** 🟡 — Different patient population, different prescriber (rheumatologists vs. oncologists), different payer dynamics. Same company, very different go-to-market.

**Verdict:** ❓ **Need more info.** The strategic question can't be answered without the biological one: does your platform's mechanism actually create therapeutic candidates in autoimmune? If yes (and a Noubar Afeyan "what would have to be true" exercise can be run honestly), 🟢. If unclear, run 1–2 small pilots before committing capital. If no, 🔴 — don't be seduced by TAM.

**Biggest single risk:** Expanding into a market your platform doesn't naturally fit, burning $50M+ on programs that fail in IND-enabling studies because the biology was never right.

### Example 4: Climate / hard tech

> **User:** "Should we build our own heat-pump installation network or partner with HVAC installers?"

**Domain:** climate hardware, deployment.
**Restated:** Build vs. partner for the customer-facing installation channel for residential heat pumps.

- **Market** 🟢 — Massive and growing (electrification mandate, IRA tax credits, replacement cycle for gas furnaces).
- **Moat** 🟡 — Building your own network could create Process Power (training, quality, speed) and Switching Costs (warranty, service). Partnering is faster but cedes the customer relationship.
- **Product** 🟢 — Painkiller (existing furnace replacement), with tax credit acting as Hormozi-style offer enhancer.
- **Distribution** 🔴 — Saul Griffith lens: this is a deployment problem. HVAC installers are the rate-limiting step nationally. Build-your-own is slow; partner is fast but creates dependency.
- **Customer** 🟡 — Homeowner is the buyer but contractor is the gatekeeper of choice. Need to win both.

**Verdict:** 🟡 **Go with conditions.** Partner-first to capture the deployment window (next 3–5 years of IRA-driven demand), but invest in proprietary installer training and quality systems so you can eventually counter-position. Build the partner network deliberately — pick installers who'll work with you exclusively in their region.

**Biggest single risk:** The installer bottleneck means even with perfect product, you can't deploy fast enough. Competitors who solve the installer-network problem win, regardless of product superiority.

---

## Notes

- **Calibrate the response to the user's stage.** A pre-PMF founder needs different evaluation than a Series C operator. Stage-shift the lenses accordingly.
- **Don't over-pattern-match.** Two consumer apps can need different lenses. Use the domain as a starting point, not a cage.
- **When the user pushes back, that's the conversation working.** Don't fold immediately — defend the reasoning or update based on new info, but don't agree just to keep them happy.
