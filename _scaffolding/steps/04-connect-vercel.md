---
step: 4
title: "Connect Vercel"
estimated_time: "5-10 minutes"
produces: "A live website that auto-deploys when you push to GitHub"
---

# Step 4: Connect Vercel

## Goal

Create a Vercel account, connect it to your GitHub repo, and deploy your starter site. After this, every push to GitHub automatically makes your site live.

## Context

Vercel is a hosting platform that watches your GitHub repo. When you push changes, Vercel automatically builds and deploys them — usually within 30 seconds. The key setting: we point Vercel at the `web-assets/` folder specifically. That means only what's in `web-assets/` goes live. Everything else (your knowledge base, content drafts, learnings) stays private in GitHub.

## Exercise

This step is entirely browser-based. Claude will give you click-by-click instructions. Follow along in your browser.

### Part A: Create a Vercel Account

1. Go to [vercel.com](https://vercel.com)
2. Click "Sign Up"
3. Choose **"Continue with GitHub"** — this automatically links Vercel to your GitHub account
4. Authorize Vercel to access your GitHub repos when prompted

Tell Claude: **"I'm signed in to Vercel."**

### Part B: Create a New Project

1. On the Vercel dashboard, click **"Add New..."** → **"Project"**
2. You'll see a list of your GitHub repos — find and select **marketing-ai**
   - If you don't see it, click "Adjust GitHub App Permissions" and grant access to the repo
3. Before clicking Deploy, look for the **"Root Directory"** setting
4. Click **"Edit"** next to Root Directory
5. Type: `web-assets`
6. Click Deploy

Tell Claude: **"Vercel is deploying."**

### Part C: Wait for Deploy

Vercel will build and deploy your site. This usually takes 30-60 seconds. You'll see a progress screen with green checkmarks.

When it's done, Vercel shows you a URL like: `marketing-ai-abc123.vercel.app`

**Click that link.** You should see the starter page you put in `web-assets/` earlier.

That page is live. On the internet. Right now.

## Verify

- Click the Vercel URL — your starter page loads
- The URL works from your phone too (try it!)
- On the Vercel dashboard, you can see "Production" with a green status

## Next

When this step is complete, say: **"Step 4 done. My site is live. Ready for step 5."**
