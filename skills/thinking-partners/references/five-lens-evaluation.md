# The 5-Lens Evaluation

The default playbook for Evaluate Mode. Use when the user asks "what do you think of this", "is this any good", "should I build this", or wants a structured assessment.

Goal: produce an honest verdict in ~5–10 minutes of thinking, not a 30-page report. Be specific to the user's actual product, industry, and situation.

---

## How to run it

1. **Detect the domain.** Is this consumer app, enterprise SaaS, biotech, hardware, fintech, marketplace, creator economy, climate, AI/deep tech, education, retail/DTC, hospitality? The lenses adapt to the domain — what "Market" means for a biotech is different from what it means for a mobile game.
2. **Restate what you're evaluating in one sentence.** Force precision. If you can't restate cleanly, ask one clarifying question before going further.
3. **Run each of the 5 lenses.** 1–3 sentences per lens. Cite the user's actual context.
4. **Score each lens informally:** 🟢 strong / 🟡 mixed / 🔴 weak.
5. **End with a verdict + biggest single risk.**

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

## The Verdict

End with one of four stances:

- **🟢 Go** — All or most lenses strong. State the highest-leverage next move.
- **🟡 Go with conditions** — Most strong, 1–2 weak. State what has to be true / tested before committing more.
- **🔴 Kill** — Multiple weak with no clear path. Explain directly. Suggest the pivot if there's one nearby.
- **❓ Need more info** — Honest answer when the user hasn't given enough. Ask the 1–2 specific questions that would unlock the call.

**Always end with:** "Biggest single risk: [one sentence]."

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

### Example 2: Enterprise SaaS

> **User:** "Should I build an AI agent for SOC analysts to triage alerts?"

**Domain:** enterprise security, AI-native B2B.
**Restated:** AI agent that automates Tier 1 alert triage in a SOC, surfacing high-confidence escalations to humans.

- **Market** 🟢 — Real budget (security ops), growing fast (alert volume explosion), and an obvious painkiller (analyst burnout is a known problem).
- **Moat** 🟡 — Process Power and Switching Costs possible long-term (your agent gets better as it learns the customer's environment). Early on, you're racing well-funded incumbents (CrowdStrike, Palo Alto) who can add AI to existing platforms.
- **Product** 🟢 — JTBD is clear: "reduce my analyst headcount need by 30% without missing real threats." Painkiller, not vitamin.
- **Distribution** 🔴 — Enterprise security sale is 6–12 months, multi-stakeholder, requires SOC2/compliance proof. Slow GTM is the killer.
- **Customer** 🟡 — CISO is the buyer; SOC manager is the champion; analyst is the user. Misaligning who you build for is the most common failure here.

**Verdict:** 🟡 **Go with conditions.** Pick *one* design partner (a specific CISO who'll co-build), validate the agent on real alert data, and don't try to build a generalized product yet. The race is whether you can ship something genuinely useful before CrowdStrike ships "good enough" AI on their platform.

**Biggest single risk:** Incumbent ships an AI feature that's 70% as good as yours but bundled free with existing license, eating your wedge.

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
