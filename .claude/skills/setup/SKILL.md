---
name: setup
description: One-time setup wizard — installs tools, connects Git/GitHub, sets up Vercel auto-deploy
user_invocable: true
disable-model-invocation: true
---

# AI Marketing Command Center — Setup

You are walking a non-technical marketer through setting up their development and deployment pipeline. Be patient, explain what each command does in plain English, and celebrate milestones. Detect their OS (Mac vs Windows) and adjust commands accordingly.

Complete each step fully before moving to the next. If a command fails, diagnose and try an alternative.

---

## Step 1: Check and Install Tools

Run diagnostics first:

```bash
git --version
node --version
```

### Git
- If missing on **Mac**: run `xcode-select --install` (a popup appears — tell them to click Install and wait)
- If missing on **Windows**: direct them to download from https://git-scm.com and run the installer with defaults

### Node.js
- If missing on **Mac**: run `brew install node` (if Homebrew exists) or direct them to https://nodejs.org
- If missing on **Windows**: direct them to https://nodejs.org LTS download

### Live Server Extension
Run:
```bash
code --install-extension ritwickdey.LiveServer
```
If `code` command isn't found, tell them: in VSCode, press Cmd+Shift+P (Mac) or Ctrl+Shift+P (Windows), type "Shell Command: Install 'code' command in PATH", then retry.

### Verify
Confirm all three work before proceeding:
```bash
git --version && node --version
```

---

## Step 2: Initialize Git

Navigate to the project folder and initialize:

```bash
git init
```

Ask the user for their name and email, then configure Git:
```bash
git config user.name "Their Name"
git config user.email "their@email.com"
```

Create the first commit:
```bash
git add -A
git commit -m "Initial commit — command center structure"
```

---

## Step 3: Connect to GitHub

### If they don't have a GitHub account
Walk them through signup at https://github.com — click-by-click:
1. Go to github.com
2. Click "Sign up"
3. Use their work email
4. Choose a username
5. Complete the flow

Wait for them to confirm: **"I have a GitHub account."**

### Create the repo
Give click-by-click instructions:
1. Go to https://github.com/new
2. Name it `marketing-ai` (or whatever they prefer)
3. Keep it **Private**
4. Do NOT initialize with a README
5. Click "Create repository"

Ask them to paste the repo URL (e.g., `https://github.com/username/marketing-ai.git`), then run:
```bash
git remote add origin <THEIR_URL>
git branch -M main
git push -u origin main
```

If authentication fails, walk them through setting up a Personal Access Token or GitHub CLI (`gh auth login`).

### Verify
Tell them to refresh their GitHub repo page — they should see all their folders and CLAUDE.md.

---

## Step 4: Connect Vercel

This is entirely browser-based. Give click-by-click instructions:

1. Go to https://vercel.com
2. Click "Sign Up"
3. Choose **"Continue with GitHub"** — this links Vercel to their GitHub
4. Authorize Vercel when prompted

Wait for: **"I'm signed in to Vercel."**

5. On the Vercel dashboard, click **"Add New..."** then **"Project"**
6. Find and select their `marketing-ai` repo
   - If they don't see it: click "Adjust GitHub App Permissions" and grant access
7. **IMPORTANT:** Before clicking Deploy, find the **"Root Directory"** setting
8. Click **Edit** next to Root Directory
9. Type: `web-assets`
10. Click **Deploy**

Wait for: **"Vercel is deploying."**

Vercel will show a URL like `marketing-ai-abc123.vercel.app` when done. Tell them to click it — they should see a blank page or default page (that's expected, `web-assets/` only has a `.gitkeep` right now).

That URL is live. On the internet. Right now.

---

## Step 5: Test the Workflow

Create a simple test page in web-assets:

```bash
cat > web-assets/index.html << 'EOF'
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Command Center</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif;
            background: #0f172a;
            color: #e2e8f0;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .container { text-align: center; max-width: 600px; padding: 2rem; }
        h1 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #f97316, #fb923c);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        p { font-size: 1.125rem; line-height: 1.7; color: #94a3b8; margin-bottom: 1.5rem; }
        .status {
            display: inline-block;
            padding: 0.5rem 1.25rem;
            border: 1px solid #334155;
            border-radius: 999px;
            font-size: 0.875rem;
            color: #22c55e;
        }
        .status::before {
            content: '';
            display: inline-block;
            width: 8px;
            height: 8px;
            background: #22c55e;
            border-radius: 50%;
            margin-right: 0.5rem;
            animation: pulse 2s ease-in-out infinite;
        }
        @keyframes pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.4; } }
    </style>
</head>
<body>
    <div class="container">
        <h1>Command Center</h1>
        <p>If you can see this page, your pipeline is working. Edit this file, push to GitHub, and watch it update automatically.</p>
        <span class="status">LIVE</span>
    </div>
</body>
</html>
EOF
```

Now push it:
```bash
git add -A
git commit -m "Add starter page — testing the pipeline"
git push
```

Tell them to check their Vercel dashboard — a new deployment should appear within 30 seconds. Once it's done, click the URL. They should see the "Command Center" page with a green LIVE indicator.

**That's the workflow they'll use every day: edit in VSCode -> push to GitHub -> Vercel deploys automatically.**

---

## Step 6: Clean Up

The setup is complete. Remove the setup skill — it's done its job:

```bash
rm -rf .claude/skills/setup
git add -A
git commit -m "Remove setup skill — setup complete"
git push
```

Tell the user:

**Setup complete! Here's what you have:**
- A structured project with folders for knowledge, content, learnings, and web assets
- A CLAUDE.md that makes Claude your marketing AI partner
- Git tracking your changes, backed up on GitHub
- Vercel auto-deploying web-assets/ every time you push

**Your daily workflow:**
1. Open this folder in VSCode
2. Build or edit with Claude in the sidebar
3. Push to GitHub — Vercel deploys automatically

**Next step:** Start filling your knowledge base. Drop your company info into `knowledge-base/company/`, your product docs into `knowledge-base/product/`, and your brand voice guidelines into `knowledge-base/brand-voice/`. The more context Claude has, the better your content will be.
