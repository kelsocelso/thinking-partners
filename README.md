# Thinking Partners

A Claude skill that turns Claude into a brain trust of legendary founders, operators, investors, marketers, strategists, and scientists spanning every major industry — consumer, enterprise, biotech, fintech, hardware, AI, climate, media, retail, education, and more.

Use it to pressure-test ideas, evaluate strategies, debate decisions, brainstorm directions, audit moats, review positioning, or just think out loud about your business — with the right lens pulled for the question instead of generic advice.

## What's inside

- **80+ thinkers** profiled with signature ideas, the questions they'd ask, and where they're most useful. Helmer, Thiel, Christensen, Bezos, Chesky, Bier, Slootman, Levie, Andreessen, Horowitz, Munger, Taleb, Hassabis, Amodei, Karpathy, Church, Afeyan, Doudna, Langer, Gawande, Fadell, Musk, Luckey, Collison, Levchin, Vélez, Gurley, LaFontaine, Drexler, Chouinard, Blakely, Weiss, Lake, Amoruso, Hewitt, Dunford, Sutherland, Godin, Raskin, Chen, Balfour, Hormozi, Ben Thompson, Mr. Beast, Meyer, Branson, Khan, Koller, and many more.
- **Six modes** the skill switches between automatically based on what you ask: Evaluate, Pressure-Test, Brainstorm, Strategic Review, Specific-Thinker, Free-Flow.
- **5-Lens Evaluation framework** (Market / Moat / Product / Distribution / Customer) that adapts to your industry — what "Market" means for a biotech ≠ what it means for a mobile game.
- **Industry playbooks** for 13 domains: consumer apps & games, enterprise SaaS, AI / deep tech, biotech, hardware, fintech, marketplaces, e-commerce / DTC, hospitality, creator economy, climate, education, plus cross-domain patterns.
- **Anti-patterns** built in: no name-parading, no yes-man answers, no fundraising lenses when the question isn't about fundraising, no tokenizing voices.

## How to use it

Once installed, the skill auto-activates when you ask Claude things like:

- "What do you think of this idea: [...]"
- "Pressure-test this for me"
- "Brainstorm with me on [...]"
- "What's my moat?"
- "How would Thiel look at this?"
- "Play devil's advocate"
- "What am I missing?"

You can also invoke it explicitly: `/thinking-partners` or `/brain-trust`.

## Installation

### Option 1: Claude.ai (web app)

1. Download the [`thinking-partners.skill`](./thinking-partners.skill) file from this repo (or [build it yourself](#building-the-skill-file-from-source) — see below).
2. Go to **claude.ai → Settings → Capabilities → Skills** (or Settings → Skills depending on plan).
3. Click **Upload skill** and select the `.skill` file.
4. Start a new chat and ask Claude something strategic — the skill should auto-activate.

**Note:** Skills are currently available on Claude Pro, Max, Team, and Enterprise plans. Check [docs.claude.com](https://docs.claude.com) for current availability.

### Option 2: Claude Code (CLI / IDE)

1. Clone this repo to your skills directory:
   ```bash
   # Project-level (only this project sees it)
   mkdir -p .claude/skills
   git clone https://github.com/kelsocelso/thinking-partners.git .claude/skills/thinking-partners

   # OR user-level (all your projects see it)
   mkdir -p ~/.claude/skills
   git clone https://github.com/kelsocelso/thinking-partners.git ~/.claude/skills/thinking-partners
   ```
2. Restart Claude Code if it was running.
3. The skill will be auto-discovered and trigger on relevant prompts.

### Option 3: Claude API / Agent SDK

Reference the skill folder when configuring your agent. See [Anthropic's docs](https://docs.claude.com) for the latest pattern — skill support in the API is evolving.

## Building the `.skill` file from source

A `.skill` file is just a zip of this folder. If you've cloned the repo and want to rebuild the upload artifact yourself:

```bash
cd thinking-partners
zip -r ../thinking-partners.skill SKILL.md references/
```

Or with Python (no zip dependency):

```bash
python3 -m zipfile -c thinking-partners.skill SKILL.md references/
```

## Repo structure

```
thinking-partners/
├── SKILL.md                          # Main skill file — modes, roster, anti-patterns
├── references/
│   ├── thinkers.md                   # Deep profiles of every thinker on the roster
│   ├── five-lens-evaluation.md       # The default evaluation framework
│   ├── moats-and-strategy.md         # 7 Powers, Porter, Thiel, Taleb
│   ├── brand-and-marketing.md        # Positioning, narrative, growth loops, offers
│   └── industry-playbooks.md         # Domain-specific lenses for 13 industries
├── thinking-partners.skill           # Pre-built artifact for Claude.ai upload
├── README.md                         # This file
└── LICENSE                           # MIT
```

## Design notes

A few intentional choices worth knowing:

1. **No master framework.** The skill picks the right tool for the question instead of running every framework on every prompt. A single rubric flattens the value of having different thinkers.
2. **Mixed naming.** Thinkers are named when their voice adds real signal, synthesized otherwise. No name-parading.
3. **Domain detection.** The skill identifies the industry first, then pulls relevant voices. Consumer-mobile frameworks don't get dragged into biotech conversations.
4. **Verdicts, not vibes.** Evaluate Mode ends with Go / Conditions / Kill / Need-info. Pressure-Test Mode ends with the sharpest single risk. Brainstorm Mode converges on 2–3 picks.
5. **Anti-yes-man.** Pushes back when ideas are weak. The skill is worthless if every answer is "great thinking!"

## Tuning

If the skill feels off in a particular direction, edit `SKILL.md`:

- **Too many names per response?** Strengthen the anti-parading note in the "How to behave" section.
- **Too soft on verdicts?** Strengthen the Verdict section in `references/five-lens-evaluation.md`.
- **Missing a thinker?** Add them to `references/thinkers.md` with their signature ideas, the questions they'd ask, and where they're most useful. Cross-reference them in the roster section of `SKILL.md`.
- **Missing an industry?** Add a section to `references/industry-playbooks.md`.

## License

MIT — see [LICENSE](./LICENSE). Use it, fork it, modify it, share it.

## Credits

Built collaboratively with Claude. The roster draws from publicly known frameworks, books, essays, and interviews of the people profiled — none of the profiles claim to quote anyone, only to channel their lens. If something feels wrong about how a thinker is represented, open an issue or PR.
