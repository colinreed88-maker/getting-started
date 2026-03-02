# Cursor Setup

This guide configures Cursor with Flow's rules, skills, agents, and brand assets. After this, every conversation with the AI will automatically follow our brand standards, code conventions, and workflow patterns.

---

## What You Are Installing

| Component | What It Does | Location |
|-----------|-------------|----------|
| **Rules** | Persistent instructions the AI always follows (brand colors, code conventions, workflow) | `.cursor/rules/` in your project |
| **Agents** | Specialized AI personas for different domains (slide decks, new project setup) | `.cursor/agents/` in your project |
| **Skills** | Interactive workflows the AI can execute (generating a PRD, scaffolding a project) | `~/.cursor/skills/` (personal, all projects) |

---

## 1. Install Rules

Rules are the most important piece. They tell the AI who we are, how we work, and what standards to follow. Without rules, the AI generates generic output. With rules, it generates Flow-branded, convention-following output from the first message.

1. Open your workspace folder in Cursor (File > Open Folder > select your project folder)
2. In the terminal (`` Ctrl+` ``), create the rules directory:

```
mkdir .cursor\rules
```

3. Copy all `.mdc` files from `getting-started-flow/config/cursor-rules/` into your project's `.cursor/rules/` folder:

```
xcopy "C:\path\to\getting-started-flow\config\cursor-rules\*" ".cursor\rules\" /Y
```

(Replace `C:\path\to\getting-started-flow` with the actual path to your getting-started-flow folder.)

### What Each Rule Does

**Always active (loaded every conversation):**
- `core.mdc` -- Flow brand colors, fonts, tone, preferences, deployment config
- `pnpm-only.mdc` -- Enforces pnpm as the only package manager
- `agent-workflow.mdc` -- Build lifecycle, planning discipline, agent delegation

**Loaded on demand (when the AI detects relevance):**
- `flow-brand-design.mdc` -- Detailed brand CSS, chart styling, and interactive features
- `creative-brainstorm.mdc` -- Structured thinking framework before creative work
- `nextjs-best-practices.mdc` -- Next.js performance and architecture patterns
- `slide-deck-creation.mdc` -- HTML slide template system

---

## 2. Install Agents

Agents are specialized AI personas. Instead of a generic assistant, you get domain experts.

1. Create the agents directory:

```
mkdir .cursor\agents
```

2. Copy the agent files:

```
xcopy "C:\path\to\getting-started-flow\config\cursor-agents\*" ".cursor\agents\" /Y
```

### When to Use Each Agent

| Agent | Use When |
|-------|----------|
| `project-launcher` | Starting a brand new project -- handles PRD, tooling audit, scaffolding |
| `deck-builder` | Creating or editing HTML slide decks, adding charts to presentations |

To use an agent, mention it in your Cursor chat: "Use the deck-builder agent to create a new slide deck."

---

## 3. Install Skills

Skills are interactive workflows. Unlike rules (which are passive instructions), skills guide the AI through a multi-step process.

1. Create your personal skills folder (this works across all your projects):

```
mkdir "%USERPROFILE%\.cursor\skills\generate-prd"
```

2. Copy the PRD skill:

```
xcopy "C:\path\to\getting-started-flow\config\cursor-skills\generate-prd\*" "%USERPROFILE%\.cursor\skills\generate-prd\" /Y
```

### Available Skills

| Skill | Trigger | What It Does |
|-------|---------|-------------|
| `generate-prd` | "Let's build something new" or "generate a PRD" | Asks structured questions, generates a Product Requirements Document, runs a tooling audit |

---

## 4. Brand Assets

Copy the font and logo files into your project so they are available for dashboards and presentations.

For a Next.js project, copy fonts to `public/fonts/`:

```
mkdir public\fonts
xcopy "C:\path\to\getting-started-flow\config\assets\fonts\*" "public\fonts\" /Y
```

Copy logos to `public/logos/`:

```
mkdir public\logos
xcopy "C:\path\to\getting-started-flow\config\assets\logos\*" "public\logos\" /Y
```

### Visual Brand Reference

Open `getting-started-flow/config/brand-guide.html` in a browser to see a visual one-pager with all Flow brand elements: color swatches, font samples, component examples, and the full Next.js/Tailwind CSS configuration you will need for any new project.

---

## Verify It Works

Open a new Cursor chat (Ctrl+L) and type:

```
What are Flow's brand colors?
```

The AI should respond with the correct hex codes: Moonlight #F3EDDF, Midnight #3D3D3D, Sunlight #E89700, etc. If it does, the rules are loaded correctly.

Then try:

```
What custom agents do I have available?
```

It should list: project-launcher and deck-builder.

---

## Next Step

Proceed to [04 - Claude Setup](04-claude-setup.md) to configure Claude Desktop with the same Flow context.
