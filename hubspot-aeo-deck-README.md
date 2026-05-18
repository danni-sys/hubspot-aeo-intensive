# HubSpot AEO Intensive — Presentation README

**File:** `hubspot-aeo-deck.html`
**Session:** HubSpot AEO Intensive · Session 1 · Foundations
**Presenter:** Marcel Santilli
**Date:** May 19, 2026
**Live URL:** [https://danni-sys.github.io/hubspot-aeo-intensive/](https://danni-sys.github.io/hubspot-aeo-intensive/)

---

## What this is

A self-contained HTML presentation — 29 slides — built for Marcel's session at the HubSpot AEO Intensive. Everything is embedded in a single file (fonts load from Google Fonts on first connection, all images are embedded). No PowerPoint, no Gamma, no Keynote. Open the URL or the file, present, done.

**Visual style:** White background, black body text, green (`#22c55e`) accents, Inter typeface. All slides scale automatically to any screen size — designed at 1280 × 720 px, scales up/down for projectors and laptops.

---

## How to present (human)

**Easiest — just use the live URL:**
Go to [https://danni-sys.github.io/hubspot-aeo-intensive/](https://danni-sys.github.io/hubspot-aeo-intensive/) on any device. Works in any modern browser, no login required.

**Offline backup:**
Download `hubspot-aeo-deck.html` and double-click it. All images are embedded — no other files needed.

**Navigation:**
- **Arrow keys** (← →) or **spacebar** to advance
- **Prev / Next** buttons at the bottom of the screen
- The counter in the bottom center shows current position (e.g. `7 / 29`)
- **F11** (Windows) or **Cmd+Shift+F** (Mac) for browser fullscreen

---

## What Marcel can edit without touching code

Open `hubspot-aeo-deck.html` in any text editor (TextEdit on Mac, or VS Code). Use **Cmd+F** to find and replace. Safe edits:

| What to change | How to find it | Notes |
|---|---|---|
| Speaker name | Search: `Marcel Santilli` | On slide 1 and slide 28 |
| Date | Search: `May 19, 2026` | On slide 1 |
| Session time | Search: `9AM PT / Noon ET` | On slide 1 |
| Any stat or copy | Search for a few words from the slide | Change only the text, not the surrounding HTML tags |
| Survey URL | Search: `ailedgrowthsurvey.com` | On slide 27 |

**Do not change** anything between `<style>` and `</style>` unless you know CSS. Do not change anything between `<script>` and `</script>`.

---

## Slide index

| # | ID | Title / Headline | Notes |
|---|---|---|---|
| 01 | `s1` | AI Forms an Opinion of You From Four Places | Title slide |
| 02 | `s2` | Speaker intro — Marcel Santilli | Credentials + CheckThat origin |
| 03 | `s_agd` | Agenda | Four sections overview |
| 04 | `s_hook` | 49.5% of brands receive zero AI mentions | Hero stat |
| 05 | `s_layer` | There's a new layer between you and buyers | AI engine logos |
| 06 | `s_hard` | Growth is getting harder, not easier | Paid/outbound declining + tool proliferation |
| 07 | `sg1` | Google Just Made It Official | Google AI guide callouts · objection handling |
| 08 | `s3` | RAG visual — Search → Retrieve → Synthesize | Simplified flow diagram |
| 09 | `s4` | The Four Surfaces | Website / Third-party / Community / PR |
| 10 | `s5` | Sphere of Influence — build order | Graphic + text split |
| 11 | `s6` | Engine chart — 83% of citations are third-party | Bar chart by AI engine |
| 12 | `s7` | Surface 01: Website (stat headline) | What to do + 76% stat |
| 13 | `s8` | Surface 02: Third-party (stat headline) | What to do + 78% stat |
| 14 | `s9` | Surface 03: Community (stat headline) | What to do + 46.7% stat |
| 15 | `s10` | Surface 04: PR (stat headline) | What to do + 82–89% stat |
| 16 | `s_iooo` | Input → Work → Output → Outcomes | Operating model |
| 17 | `s16` | The 2.8x multiplier | 4+ surfaces = citation lift |
| 18 | `s17` | Benchmark — how brands in this category perform | CheckThat scoring context |
| 19 | `s_demo` | Demo transition | "Let's look at what good looks like" |
| 20 | `s_ct` | CheckThat walkthrough | 5-step live audit |
| 21 | `sct1` | Score guide pt.1 — Website + Third-party | What to do at each score level |
| 22 | `sct2` | Score guide pt.2 — Community + PR | What to do at each score level |
| 23 | `sg2` | Everything we covered is what Google recommends | Side-by-side validation |
| 24 | `s_sbs` | Step by step — execution sequence | Left: execution / Right: strategy |
| 25 | `s18t` | 4-Surface Audit Template (full-height table) | Screenshot-ready fill-in |
| 26 | `s18` | Audit prompts — all 4 surfaces | Screenshot moment |
| 27 | `s19` | State of AI-Led Growth survey | ailedgrowthsurvey.com · June 2026 |
| 28 | `s20` | Thank you / Q&A | Hand off to Rafael |

---

## Before the session — confirm these

- [ ] Confirm session time on slide 1 (`9AM PT / Noon ET`)
- [ ] Test the live URL on the presenting device before going live

---

## For an LLM working with Marcel on edits

### Where the copy lives
All slide copy is documented in Notion: **[Deck Copy — Slide by Slide](https://www.notion.so/growthxlabs/Deck-Copy-Slide-by-Slide-3612ba60bc7481bfa7c2d72c36da46ef)**

Speaker notes and talking points are in: **[Marcel's Talking Points — Slide by Slide](https://www.notion.so/3642ba60bc74814ea575e6c85379e2eb)**

### How to make edits to the HTML
1. Read the current file at `workspaces/danni/hubspot-aeo-deck.html`
2. Find the relevant slide using the HTML comment markers — every slide starts with a comment like `<!-- ══ 07 SURFACE 01: WEBSITE ════ -->`
3. Make targeted edits using search-and-replace. Always verify the surrounding HTML tags are intact after editing.
4. After any edit: run a Python script to re-embed images as base64 and push to GitHub (see push workflow in conversation history)

### What you should know about the file structure
- **Slides** are `<div class="slide" id="sN">` blocks. Dark slides have class `slide dark`. Google guide slides use IDs `sg1` and `sg2`. Score guide slides use `sct1` and `sct2`.
- **Navigation** is handled by JavaScript at the bottom — do not modify it.
- **Styles** are all in the `<style>` block at the top — edit with care.
- **Fonts**: Inter (body), JetBrains Mono (labels/stats), Caveat (handwritten annotations) — loaded from Google Fonts.
- **Colors**: `#22c55e` green accent, `#f7f7f5` light background, `#090909` dark background (title/outro), `#0D0D0D` body text.
- **Images**: All logos and screenshots are base64-embedded in the HTML. No separate image files needed. When making edits via the GitHub interface, the images remain embedded automatically.
- **Total slides**: 28. Slide counter format is `N / 29`.

---

## Related Notion pages

- [HubSpot x GrowthX (main brief)](https://www.notion.so/growthxlabs/HubSpot-x-GrowthX-35a2ba60bc748010928cd8eda7b67d6b)
- [How to Make This Workshop Actionable](https://www.notion.so/growthxlabs/How-to-Make-This-Workshop-Actionable-35e2ba60bc7481178449e9dfdc0b5b73)
- [Marcel's Talking Points — Slide by Slide](https://www.notion.so/3642ba60bc74814ea575e6c85379e2eb)
- [Deck Copy — Slide by Slide](https://www.notion.so/growthxlabs/Deck-Copy-Slide-by-Slide-3612ba60bc7481bfa7c2d72c36da46ef)
- [Deck README — How to Use and Edit](https://www.notion.so/3612ba60bc7481ec9a08e4c3db1f462e)
