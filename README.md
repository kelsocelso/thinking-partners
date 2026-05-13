# Thinking Partners

A Claude Code plugin (and standalone skill) that turns Claude into a brain trust of legendary founders, operators, investors, marketers, strategists, and scientists spanning every major industry — consumer, enterprise, biotech, fintech, hardware, AI, climate, media, retail, education, and more.

Use it to pressure-test ideas, evaluate strategies, debate decisions, brainstorm directions, audit moats, review positioning, or just think out loud about your business — with the right lens pulled for the question instead of generic advice. **In Claude Code, the skill reads through your codebase first** so answers cite real features and architecture instead of generic startup-speak.

## What's inside

- **80+ thinkers** profiled with signature ideas, the questions they'd ask, and where they're most useful. Helmer, Thiel, Christensen, Bezos, Chesky, Bier, Slootman, Levie, Andreessen, Horowitz, Munger, Taleb, Hassabis, Amodei, Karpathy, Church, Afeyan, Doudna, Langer, Gawande, Fadell, Musk, Luckey, Collison, Levchin, Vélez, Gurley, LaFontaine, Drexler, Chouinard, Blakely, Weiss, Lake, Amoruso, Hewitt, Dunford, Sutherland, Godin, Raskin, Chen, Balfour, Hormozi, Ben Thompson, Mr. Beast, Meyer, Branson, Khan, Koller, and many more.
- **Six modes** the skill switches between automatically based on what you ask: Evaluate, Pressure-Test, Brainstorm, Strategic Review, Specific-Thinker, Free-Flow.
- **5-Lens Evaluation framework** (Market / Moat / Product / Distribution / Customer) that adapts to your industry — what "Market" means for a biotech ≠ what it means for a mobile game.
- **Industry playbooks** for 13 domains: consumer apps & games, enterprise SaaS, AI / deep tech, biotech, hardware, fintech, marketplaces, e-commerce / DTC, hospitality, creator economy, climate, education, plus cross-domain patterns.
- **Code-aware grounding (Claude Code only).** Before answering, the skill scans your README, platform manifest, and a handful of representative source files so it references your real product instead of generic startup advice.
- **Anti-patterns** built in: no name-parading, no yes-man answers, no fundraising lenses when the question isn't about fundraising, no tokenizing voices.

## Slash commands

Once installed, you can invoke it explicitly:

- `/thinking-partners <your question>` — primary entry point
- `/brain-trust <your question>` — alias

Or just ask Claude something strategic and the skill auto-activates:

- "What do you think of this idea: [...]"
- "Pressure-test this for me"
- "Brainstorm with me on [...]"
- "What's my moat?"
- "How would Thiel look at this?"
- "Play devil's advocate"
- "What am I missing?"

## Installation

### Option 1: Install as a Claude Code plugin (recommended)

In Claude Code, run:

```
/plugin marketplace add kelsocelso/thinking-partners
/plugin install thinking-partners@thinking-partners
```

That registers both the skill and the `/thinking-partners` and `/brain-trust` slash commands. Restart Claude Code (or open a new session) and you're good.

To update later: `/plugin update thinking-partners`. To remove: `/plugin uninstall thinking-partners`.

### Option 2: Manual install in Claude Code (no plugin manager)

Clone the repo and symlink the skill and commands into your `~/.claude/` directory:

```bash
git clone https://github.com/kelsocelso/thinking-partners.git ~/repos/thinking-partners

# Skill
mkdir -p ~/.claude/skills
ln -s ~/repos/thinking-partners/skills/thinking-partners ~/.claude/skills/thinking-partners

# Commands
mkdir -p ~/.claude/commands
ln -s ~/repos/thinking-partners/commands/thinking-partners.md ~/.claude/commands/thinking-partners.md
ln -s ~/repos/thinking-partners/commands/brain-trust.md ~/.claude/commands/brain-trust.md
```

For project-level install (only this repo sees it), use `.claude/skills/` and `.claude/commands/` inside your project instead of `~/.claude/`.

### Option 3: Claude.ai (web app) — skill only, no slash commands

1. Download [`thinking-partners.skill`](./thinking-partners.skill) from this repo (or [build it yourself](#building-the-skill-file-from-source) — see below).
2. Go to **claude.ai → Settings → Capabilities → Skills** (or Settings → Skills depending on plan).
3. Click **Upload skill** and select the `.skill` file.
4. Start a new chat and ask Claude something strategic — the skill auto-activates.

**Note:** Skills are currently available on Claude Pro, Max, Team, and Enterprise plans. Check [docs.claude.com](https://docs.claude.com) for current availability. The web app has no filesystem access, so the code-grounding step is automatically skipped — you'll get the strategic lenses but not the codebase-aware analysis.

### Option 4: Claude API / Agent SDK

Point the skill loader at the `skills/thinking-partners/` directory. See [Anthropic's docs](https://docs.claude.com) for the current pattern — skill support in the API is evolving.

## Building the `.skill` file from source

A `.skill` file is just a zip of the skill folder. To rebuild the upload artifact:

```bash
cd skills/thinking-partners
zip -r ../../thinking-partners.skill SKILL.md references/
```

Or with Python (no zip dependency):

```bash
cd skills/thinking-partners
python3 -m zipfile -c ../../thinking-partners.skill SKILL.md references/
```

## Repo structure

```
thinking-partners/
├── .claude-plugin/
│   ├── plugin.json                # Plugin manifest
│   └── marketplace.json           # Marketplace entry (so /plugin install works)
├── skills/
│   └── thinking-partners/
│       ├── SKILL.md               # Main skill file — modes, roster, anti-patterns
│       └── references/
│           ├── thinkers.md        # Deep profiles of every thinker
│           ├── five-lens-evaluation.md
│           ├── moats-and-strategy.md
│           ├── brand-and-marketing.md
│           └── industry-playbooks.md
├── commands/
│   ├── thinking-partners.md       # /thinking-partners slash command
│   └── brain-trust.md             # /brain-trust alias
├── thinking-partners.skill        # Pre-built artifact for Claude.ai upload
├── README.md
└── LICENSE                        # MIT
```

## Design notes

A few intentional choices worth knowing:

1. **No master framework.** The skill picks the right tool for the question instead of running every framework on every prompt. A single rubric flattens the value of having different thinkers.
2. **Code-first when possible.** In Claude Code the skill grounds itself in your actual repo before answering. Strategic advice that ignores what you've actually built is mostly noise.
3. **Mixed naming.** Thinkers are named when their voice adds real signal, synthesized otherwise. No name-parading.
4. **Domain detection.** The skill identifies the industry first, then pulls relevant voices. Consumer-mobile frameworks don't get dragged into biotech conversations.
5. **Verdicts, not vibes.** Evaluate Mode ends with Go / Conditions / Kill / Need-info. Pressure-Test Mode ends with the sharpest single risk. Brainstorm Mode converges on 2–3 picks.
6. **Anti-yes-man.** Pushes back when ideas are weak. The skill is worthless if every answer is "great thinking!"

## Tuning

If the skill feels off in a particular direction, edit `skills/thinking-partners/SKILL.md`:

- **Too many names per response?** Strengthen the anti-parading note in the "How to behave" section.
- **Too soft on verdicts?** Strengthen the Verdict section in `references/five-lens-evaluation.md`.
- **Missing a thinker?** Add them to `references/thinkers.md` with signature ideas, the questions they'd ask, and where they're most useful. Cross-reference them in the roster section of `SKILL.md`.
- **Missing an industry?** Add a section to `references/industry-playbooks.md`.
- **Code-grounding too aggressive / too shy?** Tune the budget and trigger conditions in the "Ground in the product first" section of `SKILL.md`.

## License

MIT — see [LICENSE](./LICENSE). Use it, fork it, modify it, share it.

## Credits

Built collaboratively with Claude. The roster draws from publicly known frameworks, books, essays, and interviews of the people profiled — none of the profiles claim to quote anyone, only to channel their lens. If something feels wrong about how a thinker is represented, open an issue or PR.
