# AI at Flow

## Why This Matters

Flow moves fast. We create spaces where people feel at home -- and behind the scenes, we build dashboards, presentations, internal tools, and branded experiences to keep everything running. Traditionally, building anything digital means either doing it manually in PowerPoint and Excel, or waiting for an engineering team.

AI-assisted development changes the equation. Instead of building everything by hand or filing a ticket, we describe what we want and an AI agent writes the code, applies our brand standards, and deploys the result. We review, refine, and ship.

This is not about becoming a software engineer. It is about removing the bottleneck between "I know what I need" and "here it is, live and working."

---

## The Progression

There are three levels of working with AI development tools. The goal of this guide is to get you to Level 3.

### Level 1: Prompt and Hope

You install an AI tool, type "build me a dashboard," and get something back. Maybe it works, maybe it does not. You spend hours debugging because the AI had no context about Flow's brand, our conventions, or how we like things formatted. The output looks generic and breaks in unexpected ways.

Most people stop here and conclude that AI coding tools are overhyped.

### Level 2: Structured Setup

Before writing a single prompt, you configure the AI with everything it needs to know:

- **Rules** that encode our brand colors, fonts, and formatting conventions
- **Skills** that teach the AI how to perform specific workflows (like generating a project brief)
- **Agents** that specialize in domains (slide decks, new project setup)
- **MCP servers** (connectors) that give the AI direct access to systems and browser

Now when you say "build me a page," the AI already knows to use Moonlight backgrounds, Midnight text, Poppins font, and our visual style. It deploys to Vercel automatically.

### Level 3: The Operator

At this level, you are not just using AI tools -- you are running a system. Every new project follows a structured lifecycle:

1. **Brainstorm** the idea with the AI
2. **Generate a PRD** (Product Requirements Document) that scopes the build
3. **Audit your tooling** -- does the project need any new skills or integrations?
4. **Plan** the build in phases
5. **Scaffold** the project with brand standards baked in
6. **Build** a 70% MVP, review it live, then iterate to 100%
7. **Ship** and move on to the next thing

The AI handles the code. You handle the thinking, the judgment, and the quality bar.

---

## What You Will Be Able to Do

After completing this guide, you will be able to:

- **Build branded pages and dashboards** -- internal tools, landing pages, KPI views, anything web-based
- **Create presentations** -- HTML slide decks with Flow branding, interactive charts, and polished formatting
- **Deploy to production** -- Push to GitHub, Vercel deploys automatically, review live

All of this without writing code from scratch. You describe what you need, the AI builds it, and you guide it to the finish line.

---

## The Tools

We use two primary AI tools:

**Cursor** is a code editor (like VS Code) with AI built in. You open a project, describe what you want in a chat panel, and the AI writes and edits files directly. It has access to your entire codebase, can run terminal commands, and connects to external services.

**Claude** (by Anthropic) is a general-purpose AI assistant. We use the Claude Desktop app for brainstorming, writing project briefs, and working through analysis. Claude can also read and understand large documents and complex data.

Both tools are configured with the same Flow brand standards and preferences. Whether you work in Cursor or Claude, the AI knows who we are and how we work.

---

## Next Step

Proceed to [02 - Install Tools](02-install-tools.md) to get everything installed on your machine.
