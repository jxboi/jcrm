# jCRM

A mobile-first enterprise web app where users talk to their personal AI
agent for work — with a built-in CRM added in stages.

**Status:** frontend-only UI prototype, design hill climb in progress.
**Latest (iter11):** scored 9.1/11 (blind score, Opus 5.5, live) — every
category at 9.0 or above except Imagery at 8.0 (the illustrated Jo
ceiling). Overall 9.1 ties iter10 as the best so far.

## What's in iter11

Iter11 fixes: the side-chat overflow cue now visibly shows the 5th row peeking at desktop (10.9px of text under the fade); the bottom dock stays the same height on every phone tab, so the nav no longer jumps when switching tabs (scripted-click CLS 0.0000); Jo's fur and the header shadows are softer (blurred halo, gentler gradient, broader shadows).

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
