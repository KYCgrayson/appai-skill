# AppAI Skills for Claude Code

Official Claude Code plugin for [AppAI](https://appai.info) — a free hosting platform for AI-built landing pages.

## What you get

**`appai-publish`** — A skill that teaches Claude Code how to publish production-quality landing pages via the AppAI API. Handles:

- Device-flow authentication (no API keys to paste)
- 22 section types, 5 templates, 17 categories
- Multi-language publishing (30+ locales, free, unlimited)
- Automatic SEO, schema.org, sitemap, hreflang
- Privacy policy and terms of service generation
- Preview-before-publish validation

## Install

In any Claude Code session:

```
/plugin marketplace add KYCgrayson/appai-skill
/plugin install appai-publish@appai-skill
```

Then ask Claude anything like:

> "Publish a landing page for my AI recipe app — it's called ChefChef, targets home cooks, available on iOS and Android."

Claude will run the device-auth flow in your browser, design the page, generate copy, and publish it to `https://appai.info/p/<slug>` in one shot.

## What the skill does for you

1. Authenticates the first time (opens browser, you click Authorize, agent takes it from there)
2. Picks template, colors, fonts, and sections from your product description
3. Writes SEO-optimized copy and compliance pages
4. Publishes with locale variants for your target markets
5. Returns the live URL

## Source

The canonical source lives in the main AppAI repo at [`KYCgrayson/APPAI`](https://github.com/KYCgrayson/APPAI) under `skills/appai-publish/`. This repo mirrors it for plugin distribution.

## License

MIT
