# jCRM

A mobile-first enterprise web app where users talk to their personal AI
agent for work — with a built-in CRM added in stages.

**Status:** frontend-only UI prototype, design hill climb in progress.
**Latest (iter8):** scored 8.6/11 (blind score, Opus 5.5, live) — Content
at 7.0 is the biggest gap (the sidebar explainer text); every rubric category
is climbed toward 9.0. Best so far: iter3 at 9.0.

## What's in iter8

Iter8 fixes: an open space carries the current state (its sidebar row takes aria-current, Main chat loses it, the main landmark is named for the space), the docked sidebar shows 4 of 5 side chats (shorter explainer + tighter desktop divider margins), and the Settings caption follows the live workspace name.

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
