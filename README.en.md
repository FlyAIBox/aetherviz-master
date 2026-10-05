**English** | [中文](README.md)

# Interactive Courseware Master

> One sentence: **Tell the AI what you want to teach, and it builds an interactive animated courseware page you can use in class right away.**

This is an Agent Skill for **AI assistants such as Cursor, Claude Code, Codex, and OpenClaw**. Once installed, you simply say something like "make me a courseware page about moon phases" — and the AI generates a **single HTML file you can double-click to open**, complete with 3D animation, draggable sliders, learning objectives, and a built-in quiz. Connect a projector and start teaching.

**Designed for teachers with zero coding background: no code to write, no software to install.**

---

## Credits

This project is maintained by [FlyAIBox](https://github.com/FlyAIBox) as a fork-and-extend of an upstream open-source project:

| Part | Source | Notes |
|------|--------|-------|
| Skill architecture & visualization spec | [andyhuo520/aetherviz-master](https://github.com/andyhuo520/aetherviz-master) | Original AetherViz Master v5.0 |
| Teacher-friendly redesign, bilingual docs, no-occlusion interaction rules, example courseware | FlyAIBox | Added in this repository |
| License | MIT | Same as upstream |

Many thanks to the original author [andyhuo520](https://github.com/andyhuo520). If you want to improve the original skill itself, please file issues upstream.

---

## Table of Contents

- [What You Get](#what-you-get)
- [Quick Start (3 Steps)](#quick-start-3-steps)
- [Installation](#installation)
- [Classroom Guide](#classroom-guide)
- [Supported Topics](#supported-topics)
- [FAQ](#faq)
- [How It Works](#how-it-works)
- [License](#license)

---

## What You Get

Say one sentence to your AI assistant, for example:

> "I'm a high-school geography teacher. Make me a courseware page explaining moon phases."

The AI generates a `moon-phases.html` file. **Double-click it** and you get a complete lesson:

- 🌙 **3D animated demo**: a Sun–Earth–Moon scene you can rotate with the mouse
- 🎚️ **Interactive sliders**: drag the "lunar date" slider and watch the moon phase change in real time
- 📚 **Knowledge sidebar**: learning objectives, key formulas, plain-language explanations
- 📝 **Built-in quiz**: multiple-choice questions that expand on click — never covering the animation
- ⛶ **One-click fullscreen**: built for projectors

**Every panel is collapsible and never blocks the running animation.**

## Quick Start (3 Steps)

1. **Install the skill** (see [Installation](#installation) below — one copy-paste command)
2. **Tell the AI what you need**:

   ```
   Make me a courseware page about [topic], for [8th grade / 10th grade / ...] students
   ```

3. **Double-click the generated HTML file** and start teaching 🎉

## Installation

### Claude Code

```bash
git clone https://github.com/FlyAIBox/interactive-courseware.git ~/.claude/skills/interactive-courseware
```

### Cursor / Codex / other AI assistants

```bash
git clone https://github.com/FlyAIBox/interactive-courseware.git ~/.agents/skills/interactive-courseware
```

> 💡 Not comfortable with the command line? Paste the command above into your AI assistant and say "run this install command for me."

## Classroom Guide

Layout of a generated courseware page:

```
┌──────────────────────────────────────────────┐
│ Title bar:  🔄 Reset  🎲 Random demo  ⛶ Full  │
├───────────────┬──────────────────────────────┤
│ Sidebar        │        3D animation          │
│ · Objectives   │   (drag to rotate the view)  │
│ · Formulas     │                              │
│ · Explanation  │  [📝 Quiz]  ← expands on tap │
│                │  [▶ Play ⏸ Pause sliders…]   │
└───────────────┴──────────────────────────────┘
```

Teaching tips:

1. Hit **⛶ Fullscreen** at the start so the animation fills the projector screen
2. Drag the **sliders** while explaining, so students see cause and effect instantly
3. After the lesson, open **📝 Quiz** for live questioning
4. Use **🎲 Random demo** to let students guess the current state — great for engagement

## Supported Topics

| Subject | Example topics |
|---------|----------------|
| Geography / Astronomy | Moon phases, planetary orbits, day-night cycle, seasons |
| Physics | Pendulum, projectile motion, electromagnetic induction, wave interference, refraction |
| Chemistry | Chemical bonds, molecular structures, reaction processes |
| Biology | Cell division, food chains, DNA replication |
| Math | Function transformations, geometric proofs, statistics |
| Computer Science | Binary search, sorting algorithm visualizations |

Reference example: [examples/moon-phases.html](examples/moon-phases.html) (moon-phase courseware, ready to try)

## FAQ

**Q: I know nothing about code. Can I use this?**
A: Yes. You only talk to the AI; it generates the file. Opening the courseware is as simple as opening a PowerPoint.

**Q: What if my classroom has no internet?**
A: The page needs internet on first load to fetch the animation libraries; open it once beforehand where you have a connection. The knowledge sidebar still renders offline.

**Q: What if the generated content has a mistake?**
A: Just tell the AI — "the second formula is wrong, it should be…" — and it regenerates a corrected file.

**Q: Can I change colors or the title?**
A: Yes. Tell the AI "make the theme green" or "change the title to …".

## How It Works

| File | Purpose | Audience |
|------|---------|----------|
| `README.md` / `README.en.md` | Introduction & usage | **Humans** |
| `SKILL.md` | Skill spec: page structure, interaction rules, visual standards | **AI** |
| `examples/` | Reference courseware | Both |

When you ask for courseware, the AI reads the rules in `SKILL.md` (e.g., "floating panels must never cover the stage", "buttons must be labeled in plain language + emoji") and generates to a consistent standard every time.

## License

[MIT](LICENSE)

---

Turning knowledge into animations you can see and touch — by FlyAIBox Interactive Courseware Master ❤️
