---
step: 3
title: "Git + GitHub"
estimated_time: "10 minutes"
produces: "Your marketing-ai project backed up on GitHub with version control"
---

# Step 3: Git + GitHub

## Goal

Initialize Git in your project, create a GitHub account (if needed), and push your project to GitHub. After this, your work is backed up in the cloud and ready for Vercel to deploy.

## Context

Git tracks every change you make to your files. GitHub stores a copy of your project online. This gives you two things: a backup (your laptop could die tomorrow and you'd lose nothing) and a deployment trigger (Vercel watches GitHub and auto-publishes when you push).

## Exercise

### Part A: Create a GitHub Account (if you don't have one)

If you already have a GitHub account, skip to Part B.

1. Go to [github.com](https://github.com) in your browser
2. Click "Sign up"
3. Use your work email
4. Choose a username (your name or company name works fine)
5. Complete the signup flow

Tell Claude when you're done: **"I have a GitHub account now."**

### Part B: Configure Git

Claude will set up Git with your name and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Claude will ask you for these before running the commands.

### Part C: Initialize Your Project

Claude will navigate to your marketing-ai folder and set up Git:

```bash
cd ~/marketing-ai
git init
```

Then create a `.gitignore` file that tells Git to ignore certain files (environment secrets, system files, etc.).

### Part D: First Commit

Claude stages all your files and creates the first commit:

```bash
git add .
git commit -m "Initial commit — command center structure"
```

### Part E: Push to GitHub

1. Claude will ask you to create a new repository on GitHub:
   - Go to [github.com/new](https://github.com/new)
   - Name it `marketing-ai`
   - Keep it **Private** (your knowledge base and content are proprietary)
   - Do NOT initialize with a README (you already have files)
   - Click "Create repository"
2. GitHub will show you a set of commands. Claude will run them for you:

```bash
git remote add origin https://github.com/YOUR-USERNAME/marketing-ai.git
git branch -M main
git push -u origin main
```

## Verify

- Go to your GitHub repo in the browser — you should see your folder structure
- The `knowledge-base/`, `content/`, `learnings-and-trainings/`, and `web-assets/` folders should all be there
- Inside `web-assets/` you should see `index.html`

## Next

When this step is complete, say: **"Step 3 done. Ready for step 4."**
