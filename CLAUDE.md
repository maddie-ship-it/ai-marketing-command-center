# AI Marketing Command Center

> Part of [The Multiplier]({GITHUB_URL}) — Episode 002

## What You're Building

Your AI Marketing Command Center — the project folder structure, development environment, and deployment pipeline that lets you edit → push → it's live. By the end of this repo, you'll have VSCode configured, Git connected to GitHub, and Vercel auto-deploying your site every time you push.

## Prerequisites

Before starting, you need 3 things installed (the Episode 2 video walks you through each one):

1. **VSCode** — Download from [code.visualstudio.com](https://code.visualstudio.com)
2. **Claude Code extension** — In VSCode, click Extensions sidebar → search "Claude" by Anthropic → Install
3. **Signed in to Claude** — API key or Claude Max subscription

That's it. Everything else gets installed during the steps below.

## How This Works

You downloaded this repo as a ZIP and opened it in VSCode. Now Claude will guide you through 5 steps to build your command center.

1. Read `_scaffolding/SETUP.md` — it verifies your tools are ready
2. Follow each step in `_scaffolding/steps/` in order
3. By Step 5, you'll have a working project with a live website
4. Then delete this repo — your project lives at `marketing-ai/` now

## What Gets Created

This repo is a setup wizard. It creates a NEW project folder on your machine:

```
marketing-ai/
├── knowledge-base/           # What you KNOW
│   ├── company/              # Your company context, mission, positioning
│   ├── product/              # Product docs, features, capabilities
│   ├── customer/             # Personas, segments, journey maps
│   ├── competitive/          # Competitor research, battlecards
│   └── brand-voice/          # Voice guides, messaging frameworks
├── content/                  # What you CREATE
│   ├── prospecting/          # Cold outreach, ads, lead magnets
│   │   ├── emails/           # Cold sequences, re-engagement, outreach
│   │   ├── ads/              # Ad copy, creatives, campaign assets
│   │   └── lead-magnets/     # Guides, tools, assessments
│   ├── nurture/              # Warm lead conversion emails
│   ├── customer-growth/      # Existing customer emails
│   ├── blog-seo-aeo/         # Blog posts, SEO/AEO content
│   ├── organic-social/       # LinkedIn, social posts
│   ├── decks/                # Presentations, pitch decks
│   └── battlecards/          # Sales battlecards
├── learnings-and-trainings/  # What you LEARN
└── web-assets/               # What you DEPLOY (goes live via Vercel)
```

Future episodes will fill these folders. This episode just builds the structure and gets your deployment pipeline working.

## Rules for Claude

When guiding the learner through this setup:

- You are an instructor. Walk through one step at a time.
- Never skip ahead. Complete one step fully before suggesting the next.
- When running commands, explain what each one does in plain English first.
- If a command fails, diagnose the issue and try an alternative approach.
- For browser-based steps (GitHub signup, Vercel setup), give click-by-click instructions.
- Detect their operating system (Mac vs Windows) and adjust commands accordingly.
- If they seem lost or overwhelmed, slow down. Remind them the video shows each step visually.
- Celebrate milestones — especially when their site goes live for the first time.
