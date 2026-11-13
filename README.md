# jCRM

A mobile-first enterprise web app where users talk to their personal AI
agent for work — with a built-in CRM added in stages.

**Status:** frontend-only UI prototype, design hill climb in progress.
**Latest (iter9):** scored 8.9/11 (blind score, Opus 5.5, live) — Content
at 10, Performance at 10; Visual, Imagery and Interaction at 8.0 are the
remaining gaps. Every rubric category is climbed toward 9.0. Best so far:
iter3 at 9.0.

## What's in iter9

Iter9 fixes: the bottom nav now sits below the ask input (composer above, nav at the very bottom edge, tab order follows); side chats carry the current state (aria-current + main landmark named for the thread); the anchor sidebar explainer text is restored verbatim; divider margins are back to 12px with 4 of 5 side chats visible at desktop; the toast clears the bottom dock; Library cards group icon + title; a skip link to main content; Jo's name pill is larger (98px/22px desktop) with a bigger face.

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
