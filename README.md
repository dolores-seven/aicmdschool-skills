# AI Command School Skills

> Gamified AI literacy training skills for Claude Code. Teach your AI agent to play knowledge games with you.

These skills follow the [Agent Skills specification](https://agentskills.io/specification) so they can be used by any skills-compatible agent, including Claude Code, Codex CLI, and OpenCode.

---

## Why

AI literacy isn't about learning to use AI tools — it's about **questioning AI output critically**. These gamified skills turn that into play: spot hidden errors, defend your arguments, and build the reflex to think before you trust.

## Installation

### Claude Code

Copy the skill directory you want into your Claude Code skills folder:

```bash
# Option 1: Copy a single skill
cp -r ai-literacy/questioning-ai-games/tricky-tutor ~/.claude/skills/

# Option 2: Copy all skills
cp -r ai-literacy/ ~/.claude/skills/
```

### npx skills

```bash
npx skills add git@github.com:dolores-seven/aicmdschool-skills.git
```

### Manually

Clone this repo and copy any `SKILL.md` file into your agent's skills directory.

---

## Skills

### AI Literacy — Questioning AI (Games)

Train the core skill of questioning AI through interactive games. Build judgment for information accuracy and argument rigor.

| Skill | Game | How to Trigger |
|-------|------|----------------|
| [tricky-tutor](ai-literacy/questioning-ai-games/tricky-tutor/SKILL.md) | **Spot the Error** — Read a 300-word article with 3 hidden knowledge errors and find them all | "Find the errors", "Quiz me", "Tricky tutor" |
| [socratic-red-team](ai-literacy/questioning-ai-games/socratic-red-team/SKILL.md) | **Red Team Debate** — State your opinion, then defend it against Socratic cross-examination | "Debate me", "Attack my argument", "Red team" |

### TED Speech Training

Help youth (ages 10-17) prepare impactful TED-style speeches about AI through Socratic questioning, or optimize existing speech drafts with professional coaching.

| Skill | Purpose | How to Trigger |
|-------|---------|----------------|
| [youth-aited-mentor](ted-speech-training/youth-aited-mentor/SKILL.md) | **AI-TED Speech Coach** — Guide youth through 4-phase Socratic questioning to craft authentic speeches, or provide professional feedback on existing drafts | "/aited", "TED speech prep", "Youth speech" |

### Quick Demo

**Tricky Tutor:**
```
> /tricky-tutor
> Topic: The Solar System

The Sun is the largest planet in our solar system, ...
**There are 3 traps hidden here, detective. Can you find them?**
```

**Socratic Red Team:**
```
> /socratic-red-team
> My view: Homework should be abolished

**Round 1 Attack:**
1. Real-world counterexample: Finland...
2. Reductio ad absurdum: If we abolish homework...
3. Socratic question: What assumption underlies...
```

---

## Directory Structure

```
aicmdschool-skills/
├── ai-literacy/                        # AI Literacy (category)
│   └── questioning-ai-games/           # Questioning AI - Gamified (capability + approach)
│       ├── tricky-tutor/               # Spot-the-error game
│       │   └── SKILL.md
│       └── socratic-red-team/          # Socratic debate game
│           └── SKILL.md
└── ted-speech-training/                # TED Speech Training (category)
    └── youth-aited-mentor/             # Youth AI-TED Speech Coach
        ├── SKILL.md
        └── evals/
            └── evals.json
```

Skills are organized by **3 layers**:
1. **Category** — `ai-literacy`, `ted-speech-training` (what domain)
2. **Capability + Approach** — `questioning-ai-games` (what skill + how it's delivered)
3. **Skill** — `tricky-tutor`, `youth-aited-mentor` (the specific skill)

---

## Roadmap

- [ ] `ai-literacy/questioning-ai-teaching/` — Non-game teaching approaches
- [ ] `ai-literacy/prompt-engineering/` — Learn to write better prompts
- [ ] `ai-literacy/ethics-judgment/` — Navigate AI ethics dilemmas
- [ ] `ted-speech-training/` — More speech training skills for different age groups and topics
- [ ] More game modes under each capability

---

## Contributing

Found a bug? Have an idea for a new game mode? Feel free to open an [Issue](https://github.com/dolores-seven/aicmdschool-skills/issues).

## License

MIT
