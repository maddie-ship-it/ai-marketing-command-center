# Setup Checklist

Before starting the exercises, confirm these are working:

- [ ] VSCode is open and you can see this folder in the Explorer sidebar
- [ ] Claude Code extension is installed (you should see the Claude icon in the left sidebar)
- [ ] You're signed in to Claude (click the Claude icon — you should see a chat interface, not a sign-in prompt)

## Quick Start

Open Claude in the VSCode sidebar and say:

**"I'm ready to start. Walk me through the setup."**

Claude will run a quick diagnostic to check what tools you already have, then guide you through each step.

## What Claude Will Check

Claude will run these commands to see what's already on your machine:

```bash
git --version      # Git — may not be installed yet, that's OK
node --version     # Node.js — may not be installed yet, that's OK
code --version     # VSCode CLI — should work since you're in VSCode
```

If Git or Node.js aren't installed, no problem — Step 2 handles that. If VSCode isn't responding, you may need to install the "Shell command" (Cmd+Shift+P → "Shell Command: Install 'code' command in PATH").

## How the Steps Work

There are 5 steps in `steps/`. Complete them in order:

1. **Create your project structure** — Build the marketing-ai folder layout
2. **Install missing tools** — Git, Node.js, Live Server extension
3. **Git + GitHub** — Version control and backup
4. **Connect Vercel** — Auto-deploy your site
5. **Test your workflow** — Edit → push → see it live

Each step takes 5-10 minutes. When you finish one, say: **"Step N done. Ready for step N+1."**

## If You Get Stuck

- Re-read the current step file
- Ask Claude to explain what a command does before running it
- Watch the Episode 2 video for a visual walkthrough of each step
- Take a break. You don't have to finish in one sitting.
