# Skills

A collection of **skills** for AI assistants (e.g. Claude, Cursor). This README explains what skills are, how this repo is organized, and what each folder is for.

---

## What are skills?

**Skills** are modular packages that extend an AI’s capabilities with:

- **Structured workflows** – Step-by-step procedures for specific tasks (e.g. “how to set up Tailwind in React”).
- **Domain knowledge** – Conventions, config patterns, and best practices so the AI gives consistent, correct advice.
- **Recipes and examples** – Reusable patterns (forms, tables, modals) the AI can adapt to your project.

Each skill is built around a **SKILL.md** file (with optional scripts, references, or assets). When you enable a skill, the AI loads it in relevant conversations and follows its instructions—so you get tailored help instead of generic answers.

---

## Folder layout and use cases

| Folder | Purpose | When to use |
|--------|---------|-------------|
| **`skills/`** | **Your own, ready-to-use skills.** Each subfolder is one skill (e.g. `react-tailwind`). | Install or enable these in your AI/agent so it can help with Tailwind + React, or whatever the skill describes. Share or publish these as standalone skill packages. |
| **`skills/react-tailwind/`** | **React + Tailwind CSS skill.** Install/configure Tailwind in React apps, semantic tokens, component revamp, UI recipes (forms, tables, nav, modals). | Use when you’re building or refactoring a React app with Tailwind—setup, theming, or component styling. See [skills/react-tailwind/README.md](skills/react-tailwind/README.md) for details. |
| **`.agents/skills/`** | **Agent-oriented skill sources.** May include duplicates or alternate versions of skills (e.g. `tailwind-react-ui`) and meta-skills for creating/packaging skills. | Use when your environment loads skills from `.agents/skills/` or when you’re developing or copying skills into an agent’s skill directory. |
| **`.agents/skills/skill-creator/`** | **Skill-creator meta-skill.** Teaches the AI how to design, write, and package new skills (anatomy, progressive disclosure, init/package scripts). | Use when you want to *create* or *update* a new skill—the AI follows this skill’s guidance to produce valid SKILL.md and optional resources. |
| **`.agents/skills/tailwind-react-ui/`** | **Tailwind + React UI skill** (alternate location). Same domain as `skills/react-tailwind`—Tailwind setup, tokens, component revamp, UI recipes. | Use if your setup loads skills from `.agents/skills/` and you want Tailwind+React help from this version. |

**Summary:**

- **`skills/`** = your main skill library; **`skills/react-tailwind/`** = the React + Tailwind skill (with its own README).
- **`.agents/skills/`** = agent skill sources and meta-skills (e.g. skill-creator, tailwind-react-ui).

---

## Current skill: React + Tailwind (`skills/react-tailwind/`)

This is the **React + Tailwind CSS** skill in this repo. It helps with:

- **Setup** – Installing and configuring Tailwind (and PostCSS/Autoprefixer) in CRA, Vite, Next.js, Remix, or a plain React SPA.
- **Installation order & dependencies** – Correct sequence and dependency management (Tailwind core first, then optional UI libraries).
- **Semantic design tokens** – Defining purpose-based colors, spacing, radii, and shadows in `tailwind.config` (e.g. `bg.canvas`, `text.secondary`, `border.focus`) and dark mode.
- **Component revamp** – Moving existing React components from ad-hoc CSS to Tailwind utilities and reusable patterns.
- **UI recipes** – Ready-to-adapt patterns for **forms**, **data tables**, **navigation** (top bar + sidebar), and **modals**, with accessibility in mind.
- **Troubleshooting** – Fixing “classes not applying,” production purge issues, and conflicts with other CSS.

**Quick links:**

- Full overview and how to use it: **[skills/react-tailwind/README.md](skills/react-tailwind/README.md)**
- Instructions for the AI: **`skills/react-tailwind/SKILL.md`**

Enable this skill in your AI/agent when you’re working on React projects with Tailwind so the assistant can follow the workflows and recipes above.
