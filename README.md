# jCRM

A mobile-first enterprise web app where users talk to their personal AI
agent for work — with a built-in CRM added in stages.

**Status:** frontend-only UI prototype, design hill climb in progress.
**Latest (iter12):** scored 9.1/11 (blind score, Opus 5.5, live) — every
category at 9.0 or above except Imagery at 8.0 (the illustrated Jo
ceiling). Overall 9.1 ties iter10 and iter11 as the best so far.

## What's in iter12

Iter12 is a bug fix, not a redesign: every text field in the page is now
16px (composer, sidebar search, workspace rename, space-name fields), so
iOS Safari no longer auto-zooms the page when you tap the composer — the
zoom used to cut the send button and the pipeline chevrons off the right
edge on a real iPhone. The viewport settings are untouched (user zoom
still works); nothing else changed.

- Main chat with **Jo**, an animated companion (sage-green + cream, inline
  SVG/CSS) — tap Jo to open **Today activities**
- Collapsible sidebar (drawer on phone, docked at ≥1024px) with tabs,
  side chats, search, and a Settings gear
- Floating pill **bottom navigation**: Chat, CRM, Feed, Goals, Library
- **CRM Stage 1**: pipeline board (Discovery / Proposal / Negotiation) with
  sample deals and a deal detail sheet
- **Settings**: Muse-style rows plus Workspace, Team & roles, SSO & audit
  log — every row opens a detail view; theme and notification toggles persist
- Smooth mobile-app-like motion throughout; Escape dismisses the sidebar
  and every sheet

## Run it

Open `index.html` in any browser. It's a single self-contained file —
no build step, no network requests, no backend.
