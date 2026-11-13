# jCRM

A mobile-first enterprise web app where users talk to their personal AI
agent for work — with a built-in CRM added in stages.

**Status:** frontend-only UI prototype, design hill climb in progress.
**Latest (iter10):** scored 9.1/11 (blind score, Opus 5.5, live) — every
category at 9.0 or above except Imagery at 8.0 (the illustrated Jo
ceiling). Overall 9.1 is the best so far (iter3 was 9.0).

## What's in iter10

Iter10 fixes: the toast re-places itself whenever the dock or drawer layout changes, so it never covers the composer; an open custom space survives reload; the side-chat list has a bottom fade cue at desktop (5th row peeks); chat pipeline rows get a light-grey hover fill.

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
