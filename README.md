# PoishaCount Legal

Public legal documents for the [PoishaCount](https://github.com/aminulhasan142/PoishaCount)
expense-tracker app, auto-deployed as a static site via GitHub Pages.

🌐 **Live site:** https://aminulhasan142.github.io/poishacount-legal/

## Documents

- [`privacy.md`](privacy.md) — Privacy policy

## Why this is a separate repo

The main PoishaCount source repo is private, but the privacy policy needs
to be publicly reachable at a stable URL (Google Play Console requires
one, and end-users need to view it on the web). Keeping the policy in its
own tiny public repo means:

1. The main app source stays private.
2. The policy URL never changes when the app code restructures.
3. Edits to the policy are versioned independently — every commit here is
   a privacy-policy revision.

## Editing

Plain Markdown. GitHub Pages handles the build via the `cayman` Jekyll
theme (`_config.yml`). Push to `main` → ~30 seconds later the live site
updates.
