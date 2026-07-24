---
title: White Noise Browser Extension
date: 2026-07-24T06:45:00.000-06:00
weight: 0
draft: false
summary: "The lightest-weight, open-source, most simple browser extension that
  does one boring thing: plays white noise. On/off toggle and a volume slider."
tags:
  - browser-extension
  - javascript
techstack:
  - javascript
projectLink:
  text: View on GitHub
  url: https://github.com/jonnyjackson26/white-noise-browser-extension
cover:
  hiddenInSingle: false
---
A tiny, open-source Manifest V3 Chrome extension that does exactly one boring thing: plays generated white noise. One popup, one toggle, one volume slider. No files to download, no accounts, no tracking.

**Source:** [github.com/jonnyjackson26/white-noise-browser-extension](https://github.com/jonnyjackson26/white-noise-browser-extension)

## What it does

- An on/off toggle to start and stop the sound.
- A volume slider (defaults to 35%).
- The noise is generated in the browser, so there are no audio files to load.
- Your on/off and volume settings are remembered between sessions.

## Why it's tiny

There's no build step and no framework — just plain HTML, CSS, and JavaScript. The whole thing is a popup plus a small offscreen document so audio keeps playing after the popup closes.

It requests only two permissions:

- `storage` — to save the toggle state and volume locally.
- `offscreen` — to keep audio playing once the popup is closed.

No content scripts, no remote code, no analytics, no ads, and no access to the sites you visit.

## Privacy

Nothing is collected or sent anywhere — the only things stored are your on/off setting and volume, kept locally on your own device. See the full [privacy policy](/legal/simple-white-noise-privacy-policy/).

## Try it

The extension folder loads directly as an unpacked extension: open `chrome://extensions`, turn on **Developer mode**, click **Load unpacked**, and select the `extension` folder from the repo.
