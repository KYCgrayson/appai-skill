# AppAI Skills for Claude Code

The official AppAI plugin starts at [https://appai.info/spec](https://appai.info/spec) and helps publish Hosted Pages, Wrapped tools, Connected tools, and reviewed Universal Apps.

In a Claude Code session, install with:

```text
/plugin marketplace add KYCgrayson/appai-skill
/plugin install appai-publish@appai-skill
```

Then ask, for example: "Publish a landing page for my recipe app, aimed at home cooks."

The skill follows this workflow:

1. Choose the simplest use-case that meets your needs, using your product description and audience.
2. Reuse a securely stored API key or start device authorization. The agent prints the verification link and opens it in your own browser when possible. You sign in with Google if asked, check that the code matches, and click **Approve**. The agent never approves for you or asks you to paste a key. Keys stay in memory or outside the project.
3. For a Hosted Page, read the style and logo guidance, choose a style kit and preset, and build copy and sections from current schemas. Add relevant language variants, metadata and compliance content using the specification.
4. Dry-run the page, address validation issues, and publish the same validated body. Open and check the live page at `https://appai.info/p/{slug}`, then iterate with your feedback.
5. For tools, wrap the existing deployment and use an existing owner-maintained connector when needed. For a Universal App, prepare a manifest and immutable source package, submit for AppAI review, and poll the release. Launch at `https://appai.info/app/{appId}` only once the release is approved and the production deployment is active.

AppAI does not offer arbitrary code hosting or an unrestricted upload-and-run path. Wrapped tools run on their existing hosts; agents cannot create new backends or connectors. Universal Apps follow the reviewed release process rather than becoming page sections. The skill cannot invent missing product facts or approve authorization on your behalf.

[The live specification](https://appai.info/spec) is the source of truth, with topic pages for API, style, pages, sections, languages, tools and apps. [llms-full.txt](https://appai.info/llms-full.txt) is the complete single-file fallback. This repository distributes the skill as a Claude Code plugin; the canonical source lives in [`KYCgrayson/APPAI`, under `skills/appai-publish/`](https://github.com/KYCgrayson/APPAI/tree/main/skills/appai-publish). Changes merged there are mirrored into this repo automatically.

## Updating

Users who installed an earlier version can run `/plugin marketplace update appai-skill` to get the new version.

License: MIT
