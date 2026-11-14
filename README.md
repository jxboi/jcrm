# jCRM

A mobile-first enterprise web app where users talk to their personal AI
agent for work — with a built-in CRM added in stages.

**Status:** frontend-only UI prototype, design hill climb in progress.
**Latest (iter15):** scored 9.0/11 (blind score, Opus 5.5, live) — every
category at 8.0 or above; Imagery at 8.0 (the illustrated Jo ceiling),
Interaction at 8.0 (see below). Overall 9.0, just under the iter10–iter12
best of 9.1.

## What's in iter15

Iter15 adds the Feed prompt pill the real Muse Feed tab has: a
full-width rounded pill below the "Feed" title and above the first
card, grey placeholder text ("Make me a feed about my interests. Keep
me up to date.") that truncates with an ellipsis, 16px text. Tapping
it focuses the input; submitting with Enter sends the text to Jo as a
chat message, so Jo replies — never a dead end. Empty submit sends
nothing; Escape blurs it. The cards shift down exactly the pill's
48px; the title stays put. The scorer's one new finding this round:
the suggestion chips sit behind the opaque composer at rest, so the
thread's follow-ups are invisible and unclickable on first view until
you scroll — a real defect, and the top candidate for the next
iteration.

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
