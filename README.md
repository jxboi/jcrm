# jCRM

A mobile-first enterprise web app where users talk to their personal AI
agent for work — with a built-in CRM added in stages.

**Status:** frontend-only UI prototype, design hill climb in progress.
**Latest (iter24):** scored 9.1/11 (blind score, Opus 5.5, live, on the
official rubric — target every category ≥ 9.5, not met). Layout 9,
Visual 8, Content 9, Component 9, Imagery 9, Interaction 9,
Responsive 10, Accessibility 9, Design 9, Completeness 9,
Performance 10. Overall 9.1 — a dip from the iter17–18–20–23 best
of 9.4. This is the latest of the iter22–24 batch (Jia's batch rule:
complete 3 iterations, then push once), so the live page tracks iter24
even though iter22 (9.2) and iter23 (9.4) were scored in the same batch.
The scorer's biggest gap (Visual 8 — the Jo pill's missing outline and
the title weights) did not hold against the references: the ring it saw
is our own old build's pill, the real Muse pill is borderless, and the
reference titles and row names are bold.

## What's in iter24

Iter24 finishes the batch's imagery and sidebar work. All five side chats
now sit above the sidebar footer at rest at 1440 and in the phone drawer
(row 5 clears the footer by 56px at 1440, 40px at 390), with the fade
(44px) appearing only while more is hidden below. The Library Space rows
carry illustrated icons (blue easel, blue person disc, paned window) and
the deal owners are illustrated portraits instead of initials circles;
the chat pipeline card still shows no owners. Every :hover rule now sits
inside @media(hover:hover), so taps leave no stuck fill while desktop
hover is unchanged. Jo's pill is wider and taller (111% of the avatar's
width, 39% of its height), borderless with the soft shadow kept. The
subtitle lines are gone on every tab screen and Library shows no visible
title, matching the references.

## What's in iter21

Iter21 finishes the batch's first-load work and rebuilds Library and
Goals to match their references. The dock area is solid from the
chips band's top edge to the viewport bottom, so no thread text can
show below the composer at any scroll position (verified at 375×667,
390×664, 390×844, 320×640 and 1440 open and collapsed), and the
first-load scroll is set from the available height — no text line
straddles the band's top edge at any of those sizes, and the question
stays readable below the header. Library is now a Files/Media
segmented list: Files shows the 4 saved items as flat rows with
coloured file-type art (green report icon, blue DOCX, white MD page,
dark-blue HTML), bold name, grey subtitle and a ⋮ menu; Media shows a
2-column grid of 4 illustrated thumbnail tiles; the selection and
sort-by-name persist across reload. Goals is a tracking checklist
with a green "Tracking" header, checkbox rows carrying the progress
in the grey description, and a row ⋮ menu with working "Mark done"
and "View details" (toggles persist with a strikethrough). The Jo
name pill has a visible grey hairline edge, the deal sheet's "Work on
this with Jo" aligns with the body text, a ⋯ circle sits at the
top-right of every tab screen with working menus, and the Ideas
headings run H1 → H2 → H3. The trade-offs the scorer docked: Visual
fidelity is 8.8 — the tab-screen type is about one step smaller and
denser than the references (Feed body 13px, Goals descriptions 14px,
Library subtitles 13px vs ~16–17pt), the DOCX icon draws a doubled
"W W", and the Media grid's left column sits 10px lower than the
right. And first load at 1440 with the sidebar collapsed is still
wrong: the question bubble starts 6px under the header and Jo's
closing line sits entirely behind the dock, so the pipeline card
shows with its bottom edge cut off. The ⋯ menu fades in on open but
closes instantly. (The verify suite's one recurring flag — the
clearance sweep on chip hover — was checked live by both the
orchestrator and the scorer and is not a defect: the hovered chip is
a self-contained pill 5px above the composer.)

## What's in iter18

Iter18 fixes the header smudge from iter17: the thread now opens
scrolled to the top of the latest exchange, so the question sits
readable 12px below the header at phone widths (14px at desktop),
while a new message still settles with the latest reply fully above
the chips. The chips are one scrollable row at phone widths (39px
tall, down from three stacked rows), Feed rows are tighter (114px at
phone, down from 168px) with small illustrated icons in Jo's
language and no redundant "View update" text, and Escape in Settings
now steps back to the list before closing the sheet. The trade-off
the scorer docked: at first load the last line of Jo's reply ends
40px under the chips row at 390, so the chips sit on half a line of
text next to a cut-off chip and the first screen looks clipped. The
Jo name pill is also too big — it covers the lower ~40% of the
avatar, where the reference pill only overlaps the bottom edge.
Those two are the top candidates for the next iteration. (The
verify suite's one flag — the clearance sweep on chip hover — was
checked live by both the orchestrator and the scorer and is not a
defect: the hovered chip is a self-contained pill 5px above the
composer.)

## What's in iter17

Iter17 fixes the chips-at-rest collision from iter16: the thread now
opens scrolled to the latest message (and stays that way after each
new message), so the last line of Jo's reply clears the chips by 41px
at phone width and 48px at desktop; the chips dock has a fading
backdrop so nothing shows through between the chips; the chips
left-align under Jo's message at 1440; and their labels are 14px.
Feed is now the flat hairline list from the reference — icon gutter,
no card chrome, same three updates. The trade-off the scorer docked:
scrolling to the latest on load pushes the user's opening question
bubble under the frosted header, where it shows as a grey smudge next
to Jo at every width. That is the single biggest gap and the top
candidate for the next iteration. (The verify suite's one flag — the
clearance sweep on chip hover — was checked live by both the
orchestrator and the scorer and is not a defect: the hovered chip is
a self-contained pill 5px above the composer.)

## What's in iter16

Iter16 fixes all three defects from the previous round: the suggestion
chips now sit in a pinned row above the composer (visible and clickable
at 390, 320 and 1440, light and dark, with hover feedback), the Ideas
view is three rows with hairline dividers like the reference (each row
opens a chat with Jo about that idea), and the nav glass is stronger
(36% fill, 4px blur) with a gradient active segment. The trade-off the
scorer docked: at rest the pinned chips row covers the last two lines
of Jo's reply text — the thread only clears the chips once you scroll
to the bottom. That collision is the single biggest gap and the top
candidate for the next iteration. (A first scoring run came back 9.2
but on the scorer's own paraphrased criteria — the clean staging had
missed the master rubric — so it was re-run properly; the re-run's 8.9
is the official score.)

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
