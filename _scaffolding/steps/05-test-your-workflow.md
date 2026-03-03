---
step: 5
title: "Test Your Daily Workflow"
estimated_time: "5 minutes"
produces: "A proven edit → push → live workflow you'll use every day"
---

# Step 5: Test Your Daily Workflow

## Goal

Run through the exact workflow you'll use every day: edit a file, preview it locally, push to GitHub, and watch it go live on Vercel. This is the payoff — the moment the pipeline clicks.

## Context

From now on, your daily workflow is:

1. Open `marketing-ai/` in VSCode
2. Build or edit with Claude in the sidebar
3. Preview with Live Server to make sure it looks right
4. Push to GitHub → Vercel automatically makes it live

Let's prove it works.

## Exercise

### Part A: Open Your Project in VSCode

Claude will open your marketing-ai project:

```bash
code ~/marketing-ai
```

Or: in VSCode, go to File → Open Folder → select `marketing-ai`.

You should see all your folders in the Explorer sidebar.

### Part B: Edit Your Starter Page

Open `web-assets/index.html` in VSCode.

Find the heading text and change it to something personal — your name, your company, whatever you want. This is YOUR site now.

Save the file (Cmd+S on Mac, Ctrl+S on Windows).

### Part C: Preview with Live Server

Right-click anywhere in the `index.html` file and select **"Open with Live Server"**.

Your browser opens and shows the page. You should see your changes. Every time you save the file, the browser updates automatically.

This is your local preview — only you can see it. Nothing is live yet.

### Part D: Push to GitHub

Claude will run these commands:

```bash
cd ~/marketing-ai
git add .
git commit -m "My first edit"
git push
```

That's it. Three commands. Your changes are now on GitHub.

### Part E: Watch It Go Live

1. Go to your Vercel dashboard (vercel.com)
2. You'll see a new deployment in progress (or already complete)
3. Click your site URL
4. Your changes are live. On the internet. For anyone to see.

The whole cycle — edit, push, live — takes about 30 seconds.

## Verify

- Your edited heading shows on the live Vercel URL
- The Vercel dashboard shows a successful deployment
- You understand the workflow: edit in VSCode → preview with Live Server → push to GitHub → Vercel deploys automatically

## Done

You just built your command center. You have:

- A structured project with folders for knowledge, content, learnings, and web assets
- VSCode configured with Claude and Live Server
- Git tracking your changes, backed up on GitHub
- Vercel auto-deploying your site every time you push

**This is your foundation. Every future episode builds on top of it.**

To clean up the setup repo, see `_scaffolding/CLEANUP.md`.
