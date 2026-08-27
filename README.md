# Stray Kids Wire

An independent, unofficial English-language fan hub for Stray Kids/STAY — news translation, album reviews, official-only video curation, a timezone-aware tour schedule, and a fan quiz, built to run on Google AdSense.

**Not affiliated with, endorsed by, or sponsored by JYP Entertainment or the members of Stray Kids.**

## What's in this repo

This is a single static page — `index.html` — with everything (HTML, CSS, JS) inlined. No build step, no dependencies, no backend. It's meant to be served as-is by GitHub Pages. This repo follows the same template as [Bangtan Wire](https://github.com/fhzl0117-hue/bangtan-wire) and [Blackpink Wire](https://github.com/fhzl0117-hue/blackpink-wire) — part of the "Wire" series, one dedicated site per artist.

The page is organized into six "desks," each mapped to a content pillar:

| Desk | Section id | What it does |
|---|---|---|
| 01 · News | `#news` | Translated & summarized news dispatches, each linking to its original source |
| 02 · Review | `#reviews` | Album / track reviews, text only |
| 03 · Screening Room | `#screening` | Official YouTube embeds only — never re-uploaded video |
| 04 · Signal | `#signal` | World tour schedule with a live countdown, auto-converted to the visitor's local timezone |
| 05 · Quiz | `#quiz` | A lightweight interactive quiz, no backend, no data collection |
| 06 · Market | `#market` | Links to official stores/tickets (affiliate links go here) |

## Updating content

Everything is plain HTML — open `index.html` in any editor and look for the section with the matching `id` (e.g. `<section ... id="news">`) to update copy. There's no CMS yet; each dispatch, review, or tour date is a hand-edited block. See the comments inside the `<script>` tag at the bottom for how the quiz and countdown timers work if you need to change their logic.

**Before adding new tour dates or news items**, verify the underlying facts against a real source and keep the "Read the original source" link pointing at it — that link is what keeps this page compliant with content policies (Google AdSense does not allow re-publishing copyrighted material, and this page's whole design is built around linking out and summarizing instead of reposting).

**Before adding video**, only use the standard YouTube iframe embed (`https://www.youtube.com/embed/<video id>`) pointed at an *official* channel upload. Cross-check the uploading channel via at least two independent sources (e.g. the YouTube oEmbed endpoint, `https://www.youtube.com/oembed?url=<watch url>&format=json`, plus a chart-tracking or Wikipedia source) before treating any video ID as officially sourced — a search result title claiming "(Official Music Video)" is not sufficient on its own, since fan-edit reuploads can carry the same title text. Never embed or host a re-uploaded copy.

**Photos**: intentionally, there are none. The design uses type, color, and inline SVG icons instead of photography, to avoid using copyrighted images without a license. If real photography is ever added, it must be either originally shot/owned or properly licensed — not pulled from an agency's official photo set.

## Running it locally

No build step needed — just open `index.html` in a browser, or serve the folder with any static file server, e.g.:

```
npx serve .
```

## Deploying with GitHub Pages

1. Push this repo to GitHub (or upload these files through the GitHub web UI).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch," branch `main`, folder `/ (root)`.
4. Save. GitHub will publish the site at `https://<username>.github.io/<repo-name>/` within a minute or two.
5. To attach a custom domain later: enter it in the same Pages settings screen, then add the DNS records it asks for at your domain registrar (a `CNAME` record for a subdomain like `www`, or the `A`/`ALIAS` records GitHub documents for an apex domain).

## License / ownership

Internal company project. Not licensed for redistribution outside the team without checking with whoever owns this repo.
