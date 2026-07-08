---
title: Device Frames
date: 2026-01-14T13:18:00.000-07:00
weight: 10
draft: false
summary: Open-source device frame mockups - Python/JS libraries, a REST API, and
  a web app to drop a screenshot into a real phone/tablet bezel.
tags:
  - websites
  - api
  - python
  - javascript
techstack:
  - python
  - typescript
  - fastapi
  - nextjs
projectLink:
  text: Visit Site
  url: https://device-frames-web.vercel.app
cover:
  hiddenInSingle: false
  image: /uploads/device-frames/web.gif
  alt: Screenshot framed in an iPhone mockup
---
![All Devices](https://raw.githubusercontent.com/jonnyjackson26/device-frames-media/refs/heads/main/docs/cover.png)

![Before and after applying a device frame](/uploads/device-frames/apply_frame.png)

A small ecosystem of open-source tools for putting a screenshot inside a real device bezel (iPhone, iPad, Pixel, Galaxy, etc.) - as a Python function, a JS/Node function, a REST API, or a point-and-click web app.

**Try it:** [device-frames-web.vercel.app](https://device-frames-web.vercel.app/)

## The pieces

**[device-frames-media](https://github.com/jonnyjackson26/device-frames-media)** is the foundation - a growing library of frame/mask PNGs and JSON metadata (screen coordinates, frame size, hex color) for dozens of iPhone, iPad, Pixel, and Galaxy models. Everything else pulls its assets from here at runtime, so new devices show up everywhere without a version bump.

![Frame, mask, and metadata for a device](/uploads/device-frames/frame-template-mask.png)

**[device-frames-core](https://pypi.org/project/device-frames-core/)** - Python library. repo is [device-frames-core](https://github.com/jonnyjackson26/device-frames-core)
```
pip install device-frames-core
```

**[device-frames](https://www.npmjs.com/package/device-frames)** - the JS/Node port (npm package is named `device-frames`, repo is [device-frames-js](https://github.com/jonnyjackson26/device-frames-js)). Uses `sharp` for compositing.
```
npm install device-frames
```


**API** - a FastAPI wrapper around the Python library, for anyone who'd rather hit an HTTP endpoint than install a package. Hosted on fly.io. Docs at [device-frames-api.fly.dev/docs](https://device-frames-api.fly.dev/docs). [See it on GitHub](https://github.com/jonnyjackson26/device-frames-api)

**[device-frames-web](https://github.com/jonnyjackson26/device-frames-web)** - the Next.js app at [device-frames-web.vercel.app](https://device-frames-web.vercel.app/). Upload a screenshot, pick a device, download the framed result. Also has a [browsable gallery](https://device-frames-web.vercel.app/frame-media) of every frame/mask in device-frames-media.
