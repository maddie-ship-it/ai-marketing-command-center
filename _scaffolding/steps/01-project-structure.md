---
step: 1
title: "Create Your Project Structure"
estimated_time: "5 minutes"
produces: "A marketing-ai/ folder with organized subfolders for your entire command center"
---

# Step 1: Create Your Project Structure

## Goal

Create the folder structure that will hold your entire AI Marketing Command Center. This is the foundation everything else builds on.

## Context

Most marketers keep everything in a messy Google Drive or scattered across tools. Your command center is different. It's a structured project folder where every piece of marketing knowledge, content, and web asset has a home. AI works dramatically better when it can find what it needs.

## Exercise

### Part A: Choose Your Location

Claude will ask you where you want your project folder. The default is your home directory:

- **Mac:** `~/marketing-ai/`
- **Windows:** `C:\Users\YourName\marketing-ai\`

If you want it somewhere else, just tell Claude.

### Part B: Create the Folders

Claude will create the full structure for you:

```
marketing-ai/
├── knowledge-base/
│   ├── company/           # Your company context, mission, positioning
│   ├── product/           # Product docs, features, capabilities
│   ├── customer/          # Personas, segments, journey maps
│   ├── competitive/       # Competitor research, battlecards
│   └── brand-voice/       # Voice guides, messaging frameworks
├── content/
│   ├── prospecting/       # Cold outreach, ads, lead magnets
│   │   ├── emails/        # Cold sequences, re-engagement, outreach
│   │   ├── ads/           # Ad copy, creatives, campaign assets
│   │   └── lead-magnets/  # Guides, tools, assessments
│   ├── nurture/           # Warm lead conversion emails
│   ├── customer-growth/   # Existing customer emails
│   ├── blog-seo-aeo/     # Blog posts, SEO/AEO content
│   ├── organic-social/    # LinkedIn, social posts
│   ├── decks/             # Presentations, pitch decks
│   └── battlecards/       # Sales battlecards
├── learnings-and-trainings/  # Frameworks, expert advice, captured trainings
└── web-assets/            # What goes LIVE (deploys via Vercel)
```

### Part C: Copy the Starter Site

Claude will copy the starter HTML page from this repo into your new `web-assets/` folder. This gives you something real to deploy in Step 4.

## Verify

- Open Finder (Mac) or File Explorer (Windows) and navigate to your marketing-ai folder
- You should see `knowledge-base/`, `content/`, `learnings-and-trainings/`, and `web-assets/`
- Inside `web-assets/` you should see `index.html`

## Next

When this step is complete, say: **"Step 1 done. Ready for step 2."**
