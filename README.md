# jCRM

A mobile-first enterprise web app where users talk to their personal AI
agent for work — with a built-in CRM added in stages.

**Status:** frontend-only UI prototype, design hill climb in progress.
**Latest (iter14):** scored 8.9/11 (blind score, Opus 5.5, live) — every
category at 8.0 or above; Imagery at 8.0 (the illustrated Jo ceiling),
Component and Completeness at 8.0 (Feed prompt pill and Ideas rows
still missing). Overall 8.9, just under the iter10–iter12 best of 9.1.

## What's in iter14

Iter14 makes the bottom nav pill translucent glass, the same treatment
class as iter13's header fix: the pill is white at 48% with a faint
border and 9px blur, so content scrolling behind it shows through
blurred, as in the real Muse Feed and Ideas tabs. The dock floats over
the scrolling content and `main` runs the full viewport height behind
it, with bottom padding compensating — at rest nothing moves: nav,
dock, composer and thread sit exactly where iter13 had them. The
composer input stays opaque white, and the glass works in dark theme
too. The one honest limit: the Feed tab is too short for anything to
pass under the nav, so the glass only reads on Chat and wherever
content actually scrolls.

## What's in iter13

Iter13 is a header fidelity fix, from Jia comparing the Jo header
against the real Muse header: the ring around Jo's circle is gone (a
plain white disc now, as in Muse); the Jo name pill is translucent
glass with a faint light border and blur; the pill sits 8px higher,
overlapping the bottom of Jo's drawn body; and the header floats over
the page content with a blurred backdrop instead of sitting on flat
white. Jo herself is unchanged, and nothing else moved — the thread
sits exactly where it did in iter12.

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
