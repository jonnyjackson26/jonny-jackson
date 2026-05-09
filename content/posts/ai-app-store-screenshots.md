---
draft: false
showCodeCopyButtons: true
title: AI App Store Screenshots
date: 2026-05-09T10:00:00.000-06:00
weight: -998
summary: A canvas-based editor for designing App Store and Play Store screenshots with AI-assisted copy and layout suggestions.
techstack:
  - nextJS
  - react
  - typescript
  - openai
showPostNavLinks: true
tags:
  - websites
  - ai
projectLink:
  text: Visit Site
  url: https://ai-app-store-screenshots.vercel.app/
cover:
  image: /uploads/ai-app-store-screenshots/demo.png
  alt: AI App Store Screenshots demo
  relative: false
  hiddenInSingle: false
---
[***ai-app-store-screenshots.vercel.app***](https://ai-app-store-screenshots.vercel.app/) is a canvas-based editor for designing the marketing screenshots that appear on the Apple App Store and Google Play Store listings. Drop in a screenshot of your app, pick a template, and the AI helps with the headline, subheading, and layout — so you can ship a polished store listing without hiring a designer.

{{< youtube UvV-T6Zl3dA >}}

**Important Links:**

[Live web app](https://ai-app-store-screenshots.vercel.app/) hosted on Vercel  
[GitHub repo](https://github.com/jonnyjackson26/ai-app-store-screenshots)  
[Demo video](https://youtu.be/UvV-T6Zl3dA)  

The editor is built on Fabric.js for the canvas layer, with a Next.js + React + TypeScript frontend and Shadcn UI components. State is managed with Zustand, server data with TanStack Query, and image uploads run through UploadThing. The AI features call OpenAI to suggest copy and layout based on a short description of your app. The whole project is open source under AGPL v3, so you can self-host with your own OpenAI key.
