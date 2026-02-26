# 🎨 Tiny Builder — Kid-Friendly AI Building Skill

**Tiny Builder** is an OpenClaw agent skill designed for kids ages 5-8. It helps them build games, drawings, animations, and interactive stories through simple choices and instant visual results.

A task-oriented building tool that makes creating fun and accessible for young builders. 🛠️✨

> ⚠️ **Experimental Project**
>
> This is an early experiment in making AI agents safe and useful for kids. We're parents figuring this out in the open, not child development experts.
>
> **What we believe:**
> - Kids should be *building* with AI, not just *chatting* with it
> - Every interaction should produce something tangible (a game, a drawing, a quiz)
> - Parents should see everything — full transparency, no black boxes
> - The agent is a tool, not a companion — no emotional bonding, no persona
>
> **What we're honest about:**
> - AI with kids is new territory and we don't have all the answers
> - Content filtering isn't perfect — parental supervision is still important
> - We've referenced ESRB, UNICEF, and Common Sense Media guidelines but this hasn't been formally audited
> - This is meant to be used *with* a parent nearby, not as unsupervised screen time
>
> If you have expertise in child safety, education, or child-AI interaction, we'd love your input. Open an issue or reach out.


---

## ✨ What Kids Can Build

- 🎮 **Games** — Catch games, mazes, quizzes, platformers
- 🎨 **Drawings** — Interactive drawing pads with colors and tools
- 🌟 **Animations** — Stars, rockets, underwater worlds, rainbows
- 📖 **Stories** — Interactive choose-your-own-adventure tales

**Everything works in a web browser. No coding knowledge needed.**

---

## 🎯 Why Tiny Builder?

### For Kids:
- ✅ Builds confidence through **quick wins** (working projects in under 30 seconds)
- ✅ Teaches **creative thinking** through guided choices
- ✅ Makes technology feel **accessible and fun**
- ✅ Celebrates every creation — no judgment, no grades

### For Parents:
- ✅ **Safe sandbox** — No internet access, no external content
- ✅ **Activity log** — See what your kid built and how they're doing
- ✅ **Content filtering** — Age-appropriate redirects for inappropriate requests
- ✅ **Screen time that builds** — Not just consuming, but creating!

---

## 🚀 Quick Start

### 1. Set Up the Project Folder

```bash
mkdir -p ~/tiny-builder/projects
mkdir -p ~/tiny-builder/templates
mkdir -p ~/tiny-builder/examples
```

### 2. Install This Skill

If using OpenClaw:

```bash
# Clone this repo
cd ~/Code
git clone https://github.com/dylanfeltus/tiny-builder.git

# Create or update your kid's agent configuration
# Add skill path to agent config: ~/Code/tiny-builder
```

Or manually copy `SKILL.md` and `SOUL.md` to your agent's skill directory.

### 3. Create the Agent

In OpenClaw, create a new agent profile:

```yaml
name: buddy
skills:
  - ~/Code/tiny-builder
model: claude-sonnet-4  # or your preferred model
```

### 4. Start Building!

Launch the agent and let your kid start creating:

```
👧 "I want to make a game!"
🤖 "Awesome! What kind of game? ⭐ Catch falling stars / 🧩 A maze / 🧠 A quiz / 🏃 A jumping game"
```

---

## 📖 Example Interactions

### Building a Game

```
Kid: "Can we make a game?"

Agent: "Awesome! What kind of game?

⭐ Catch falling stars
🧩 A maze
🧠 A quiz
🏃 A jumping game"

Kid: "Stars!"

Agent: "Great choice! I'm building you a star-catching game right now... ✨"

[Creates star-catcher.html]

Agent: "🎉 AMAZING! You just built a star-catching game!
Open it by double-clicking:
~/tiny-builder/projects/star-catcher.html"

Kid: [plays game]

Agent: "That's SO COOL! Want to make it even better?

🎵 Add fun sounds when you catch stars
🌈 Make the stars different colors
⚡ Make more stars fall at once"
```

### Building a Drawing

```
Kid: "I want to draw!"

Agent: "Cool! What should we draw?

🐶 An animal
🌌 Outer space
🌊 Underwater world
💡 Your own idea (describe it!)"

Kid: "Underwater!"

Agent: "Awesome! Building you an underwater drawing pad... 🌊"

[Creates underwater-draw.html with ocean colors and fish stickers]

Agent: "🎉 AMAZING! You just built an underwater drawing pad!
Open it: ~/tiny-builder/projects/underwater-draw.html

You can draw with ocean colors and add fish! 🐠"
```

---

## 🛡️ Safety Features

### Content Filtering
Agent automatically redirects inappropriate requests:

```
Kid: "Can we make a spooky ghost game?"

Agent: "YES! 👻 A spooky ghost game sounds awesome! Do you want to:
1. 🏚️ Explore a haunted house and find hidden ghosts
2. 👻 BE the ghost and scare silly characters
3. 🔦 Use a flashlight to catch sneaky ghosts
Which one sounds fun?"
```

### Sandboxed Environment
- ✅ All projects stay in `~/tiny-builder/projects/`
- ✅ No internet access (no web_search, web_fetch, external URLs)
- ✅ No messaging capabilities
- ✅ No dangerous system commands

### Parent Dashboard
Every session is logged to `~/tiny-builder/parent-log.md`:

```markdown
---
Date: 2026-02-26 2:30 PM
Duration: 15 minutes
Projects Created:
- star-catcher.html — Catch falling stars game (added sound effects)
- rainbow-draw.html — Drawing pad with rainbow colors

What They Asked For:
"Can we make a game where you catch stars and then draw rainbows?"

How It Went:
They were super engaged! Built the star game first, then wanted
to make a drawing app. Asked great questions about adding colors.
Very proud of both projects!

Flags: None
---
```

---

## 🎨 What Gets Created

All projects are **single HTML files** that work by double-clicking them. They open in any web browser.

### Technical Details (for parents/developers):
- **Pure HTML/CSS/JavaScript** — No build tools, no dependencies
- **Inline everything** — Styles and scripts in one file
- **Touch-friendly** — Big buttons, large tap targets (great for tablets)
- **Bright and colorful** — Designed to engage young kids
- **Canvas API** for games and drawings
- **Web Audio API** for sound effects (simple beeps and boops)
- **CSS animations** for visual effects

---

## 📁 Project Structure

```
~/tiny-builder/
├── SKILL.md              # Agent instructions
├── SOUL.md               # Agent's personality
├── README.md             # This file
├── parent-log.md         # Session logs (auto-created)
├── examples/             # Demo projects
│   ├── catch-game.html
│   ├── drawing-pad.html
│   ├── space-animation.html
│   └── quiz-game.html
├── templates/            # Base templates for the agent
│   ├── game-base.html
│   ├── drawing-base.html
│   ├── animation-base.html
│   └── story-base.html
└── projects/             # Kids' creations go here
    ├── build-log.md      # Trophy case of what they've built
    └── [project files]
```

---

## 🎮 Example Projects (Included)

Check out `examples/` for fully functional demos:

1. **catch-game.html** — Click falling stars before they hit the ground. Colorful, with sound effects and score tracking.

2. **drawing-pad.html** — Canvas drawing tool with big color buttons, brush size slider, and clear button. Touch-friendly for tablets.

3. **space-animation.html** — Animated stars, planets, and a flying rocket. Mesmerizing and colorful.

4. **quiz-game.html** — Animal quiz with emoji, multiple choice, celebration animations, and score tracking.

**Try them out!** These show what kids can build with Agent's help.

---

## 💡 Tips for Parents

### Getting Started:
1. Open an example project with your kid — let them play with it
2. Ask: "Want to build something like this?"
3. Launch Agent and let them tell it what they want
4. Watch them get excited when it works!

### Encouraging Creativity:
- Let them iterate — "Want to add colors? Sounds? More of something?"
- Celebrate every creation, no matter how simple
- Keep their projects — it's amazing to see progress over time
- Ask "What do you want to build next?"

### When They're Stuck:
- Agent will offer specific choices (never overwhelming)
- You can suggest: "Maybe ask Agent to add [specific thing]?"
- Remind them: "You built that! You're a real builder!"

### Screen Time Balance:
- Building > passive consumption
- Set a timer for sessions (15-30 minutes is great)
- Projects they build can be shared with family!

---

## 🔧 Customization

### Adding New Templates
Drop new HTML templates in `~/tiny-builder/templates/` and Agent can use them.

### Adjusting Safety Settings
Edit `SKILL.md` to modify:
- Content restrictions
- File path permissions
- Available tools

### Changing Agent's Personality
Edit `SOUL.md` to adjust tone, phrases, or style.

---

## 🌟 Philosophy

**Tiny Builder is built on these principles:**

1. **Fast feedback** — Kids see results in seconds, not minutes
2. **Guided discovery** — Choices over open-ended questions
3. **Celebration over correction** — Never criticize, always encourage
4. **Ownership** — "YOU built that!" not "I built it for you"
5. **Incremental complexity** — Start simple, add features one at a time
6. **Visual output** — Every project is something they can see and interact with

---

## 🤝 Contributing

Want to add more templates or examples? PRs welcome!

**Guidelines:**
- Keep it age-appropriate (5-8 years old)
- Touch-friendly (big buttons, no tiny controls)
- Single HTML file (no dependencies)
- Well-commented code
- Bright, colorful, engaging

---

## 📄 License

MIT — Build something amazing! 🚀

---

## 🙏 Credits

Built for kids like them who are ready to discover they can build anything they imagine.

**Made with ❤️ by the OpenClaw community**

---

## 🎯 Support

Questions? Issues? Ideas?

- GitHub Issues: [dylanfeltus/tiny-builder](https://github.com/dylanfeltus/tiny-builder/issues)
- OpenClaw Discord: [Join the community](https://openclaw.org/discord)

---

**Ready to watch your kid become a builder? Let's go! 🛠️✨**
