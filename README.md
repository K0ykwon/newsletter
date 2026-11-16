# Technology Newsletter

A standalone Korean editorial app covering Dev, AI, and QPU. Public output lives at https://k0ykwon.github.io/apps/newsletter/ . This repository is the source of truth; the portfolio contains a published copy of `dist/` only.

## Build and test

Node.js 22 or later:

```
npm ci
npm test
npm run build
```

Serve `dist/` with any static server. The app supports field filtering, search, permanent article URLs, native MathML formulas, responsive layouts and system dark mode. It has no analytics, backend, tracking or runtime CDN dependencies.

## Editorial workflow

Articles are JSON files in `content/`. The compiler includes **only** articles whose `approved` field is exactly `true`. A new article must remain unapproved until the owner explicitly approves that particular edition. Approval is editorial, not an automatic consequence of the schedule. Public copy must not include personal project advice, private source links or the private-chat tomato signature.

The initial release contains the three explicitly approved 2026-11-15 editions. Descriptions of research distinguish author-reported evidence from independent verification. General-reader explanatory examples are not claimed as published experimental results.

## Publication

Run tests and build, then copy the complete `dist/` directory into `K0ykwon/k0ykwon.github.io/apps/newsletter/` on a dedicated branch. Review the diff and merge only after the edition has publication approval. Never copy private Space documents or raw exports. `publication.json` records the published edition inventory. No cross-repository access tokens or automatic write credentials are configured.
