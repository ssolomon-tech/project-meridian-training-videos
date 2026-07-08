# Project Meridian — CAM Tutorial Videos (Public Hosting)

This repo exists solely to host video files for Project Meridian's CAM tutorial
series so they can be embedded directly in the tool via `<video>` tags.

**Why a separate public repo:** the main `project-meridian` repo is private,
which is correct for the codebase and any partner-specific tooling. But a
private repo's content requires GitHub session authentication, and browsers
don't send that authentication cookie on cross-origin `<video src>` requests
(only on top-level navigation) — so embedded playback on the tool's own page
was silently failing. Public repo content has no auth requirement at all, so
embedding just works. Everything here is generic tutorial content using
entirely fictional example data (Meridian Cyber Solutions doesn't exist,
created solely for training) — there's no real partner or business data in
this repo, which is what makes making it public a reasonable tradeoff.

**Source of truth:** the actual project documentation, source docs, and
`build_guide.py` used to generate the content these videos are based on all
live in the private `project-meridian` repo. This repo is a dumb file host --
nothing here should be edited directly; regenerate the video in NotebookLM
and re-upload here if a video needs to change.

## Structure
- `videos/` — the actual `.mp4` files, named `01_...` through `07_...`
- `thumbnails/` — a representative frame (or a "coming soon" placeholder) for each video, used as the card thumbnail in the tool
- `videos/Platform_Overview_Demo.mp4` — a separate, non-numbered video: a single ~4-minute walkthrough covering *both* tools together, linked from the main landing page (`tools/Landing_Page.html`) rather than either tool's own tutorial series. Real screen recording (not NotebookLM-generated), narrated over live use of both tools with the same fictional fixture data as everything else in this repo — no real partner/customer data.

## Status

| # | Video | Status |
|---|---|---|
| 1 | Welcome & the Tool Map | Live |
| 2 | Research: Intelligence & Contacts | Live |
| 3 | Discovery Part 1: Desk Research & Organization | Live |
| 4 | Discovery Part 2: Alignment & SE Supplement | Live |
| 5 | Commitment, Sign-Off & the Business Plan | Live |
| 6 | GTM Plan, Enablement Plan & Generate | Live |
| 7 | Save, Load & Handoff | Live |
| — | Platform Overview Demo (both tools, landing page) | Live |
