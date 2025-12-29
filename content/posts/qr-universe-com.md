---
title: QR-Universe.com
date: 2025-10-30T19:36:00.000-10:00
weight: 33
draft: false
summary: A dynamic QR code management tool
tags: []
techstack:
  - NextJS
  - Supabase
cover:
  hiddenInSingle: false
  image: /uploads/qr-universe.png
  alt: QR Code page
---
\### QR Universe

\*\*Tech Stack:\*\* Next.js, Supabase, Resend





QR Universe is a full-featured platform that lets users create, customize, and manage dynamic QR codes. Users can edit, download, and track analytics for each QR code. The site features a sleek dark mode and is fully optimized for both mobile and desktop.

I know there’s already many dynamic QR code websites out there, but here are some things that set my service apart:

\* I use supabase anonymous auth to make it so users can create fully dynamic QR codes without needing to log in. These codes are automatically deleted after a certain time unless they create an account, under which case I transfer those QR codes to the users real account and remove their expiration. Signing in/providing an email is a huge barrier for entry for something so simple as creating a QR code.

\* When it comes time to actually sign up, it’s as seamless as can be. I create and store OTPs of 6 random digits and send them with Resend. Users log in / sign up within seconds and with as little friction as possible.

\* All features are free out of the box: Analytics tracking, advanced QR codes like for App Store listings, downloading or viewing scan logs, etc. Other services charge for these as an upgrade requiring a monthly subscription. QR-Universe.com offers them all for free. We want to keep creating QR codes simple and free for everyone, but to maintain it costs money. For bigger teams or users, we monetize by allowing unlimited scans on specific QR codes that can be unlocked for a one time payment of 6 dollars.
