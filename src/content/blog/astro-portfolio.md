---
title: "Building a Portfolio Site Using Astro in 24 Hours"
description: "From zero to a live, high-performance portfolio using Google AI Studio, Antigravity, and Vercel."
date: "2026-05-04"
tags: ["Astro", "Antigravity", "Vercel", "AI"]
---

## Intro

How to implement a dark theme that actually helps user concentration and reduces eye strain.
They say the best time to build a portfolio was three years ago. The second best time is today—especially when you can do it in under 24 hours. As a **Python Maximalist** and an engineer who values speed without sacrificing control, I wanted a site that was blazing fast, SEO-optimized, and easy to maintain.

Here’s exactly how I wired the whole thing together—and how I overcame the AI's refusal to play nice.

---

## Phase 1: The Vision & The Google Studio "Refusal"

I started in **Google AI Studio**. My goal was simple: Use the most advanced LLMs to scaffold a modern Astro project.

**The Initial Prompt:**

> "Build me a professional portfolio using Astro 6 and Tailwind CSS. It should have sections for Tech, Investing, and 'Stuff'. Use a dark theme with 'Electric Purple' accents."

**The Roadblock:** Google AI Studio was great at generating code snippets, but when it came to the **Build/Preview** stage, it stalled. It refused to spin up the Astro dev server, giving me the dreaded "White Screen of Death" or "Internal Error." In 2026, many cloud-based builders still struggle with the complex dependencies of Astro’s new Content Layer.

**The Fix:** I realized that for a project this technical, I needed to get out of the browser. I stopped asking the AI to _run_ the code and started asking it to _write_ the code for a local environment.

---

## Phase 2: Moving to Antigravity

This is where the "Antfolio" was actually born. I moved the project into **Antigravity** to gain full control over the file system.

**The Troubleshooting Prompt:**

> "Google Studio is failing to render the preview. Let's move this locally. Give me the `package.json` for an Astro 6.2.1 project and help me fix the `legacy-peer-deps` conflict with Tailwind v4."

**The Breakthrough:** Antigravity’s Agent identified that the latest Tailwind and Astro versions were clashing on peer dependencies. Instead of me spending hours on StackOverflow, the Agent gave me the secret command that saved the project:

Bash

```
npm install --legacy-peer-deps
```

Suddenly, `npm run dev` worked. The site was alive on my Ryzen 7040.

---

## Phase 3: Deployment to Vercel

A portfolio doesn't exist until it has a URL. I chose Vercel for its speed, but even here, we had one more hurdle: the build was failing in the cloud because it didn't know about our "Legacy Peer Deps" rule.

**How we overcame the Build Error:** I didn't just click "Deploy." I had to override the Vercel Install Command on the setup screen:

1. **Toggle "Install Command" to Override.**
    
2. **Enter:** `npm install --legacy-peer-deps`
    

---

## 🚀 The "Zero-Dashboard" Push

One of the coolest features of this setup is the **Antigravity Vercel Plugin**. I now have a direct line from my editor to my live site.

**How to push directly from Antigravity:**

1. **The Plugin:** I ran `npx plugins add vercel/vercel-plugin`.
    
2. **The Terminal:** `npx vercel login` to link my laptop.
    
3. **The Final Command:** Now, I just run:
    
    Bash
    
    ```
    npx vercel --prod
    ```
    
    _The Agent then handles the zipping, uploading, and deployment in under 45 seconds._
    

---

## Final Thoughts

Building a site shouldn't be a month-long project. By leveraging AI agents and a "content-first" framework like Astro, I was able to go from a blank folder to a live site in a single day—despite the cloud builders trying to stop me.

Now, with the infrastructure out of the way, I can get back to what matters: **Tech, Investing, and suffering through Arsenal matches.**
