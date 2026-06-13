# 🔥 Ember — Systematic Review Triage

A free, browser-based tool for the **search and screening** stages of a systematic review. Search millions of papers, rank them by your own relevance criteria, screen with one click, validate your search, and export straight to ASReview — **no install, no account, no cost.** It runs entirely in your browser.

> **▶ Live demo: https://naemyoaungkhing.github.io/ember/**

Ember uses the open **[OpenAlex](https://openalex.org)** scholarly database (CC0) as its search engine. It's the *review workflow* on top of that data — the part a plain search engine doesn't give you.

## What it does

- **Search** — build a query from concept keyword groups (`OR` within a group, `AND` between groups), with year / language / type filters.
- **De-duplicate** — automatically, by DOI and normalised title.
- **Rank by relevance** — a transparent, editable keyword score (core / context / noise terms), with matched words highlighted so you see *why* a paper ranked.
- **Screen** — include / maybe / exclude per record, with keyboard shortcuts (`i` / `m` / `x`, arrows to move) and an Auto-suggest pass.
- **Validate your search** — paste DOIs of papers you *know* should be found; Ember tells you if your query is sensitive enough (and whether a missed paper is in OpenAlex at all).
- **Live PRISMA flow** — identified → de-duplicated → screened → included counts, ready for your methods chapter.
- **Multi-database merge** — import Scopus / Web of Science / PubMed exports (`.ris` / `.csv`) and merge + de-duplicate with the OpenAlex set.
- **Reproducibility** — copy a dated search record + methods paragraph, and a shareable link that reopens your exact search setup.
- **Export** — RIS for **ASReview**, worksheet/included CSVs, an open-access download hub, and save/load sessions.

## How to use

1. Open the page (or the live demo link).
2. **Step 1 — Build your search:** enter keywords, set filters, click **Fetch & rank**.
3. **Step 2 — Screen:** tune the scoring terms if needed, then triage with the buttons or keyboard.
4. **Step 3 — Hand off:** export RIS and import into [ASReview](https://asreview.nl) for AI-assisted screening.
5. **Step 4 — Export & reproduce:** save CSVs, the PRISMA record, and a shareable link.

## Scope (honest)

Ember covers the **identification and screening** front end of a systematic review (PRISMA steps 3–4). Data extraction, quality/risk-of-bias appraisal, and synthesis/meta-analysis are out of scope — use dedicated tools (ASReview, RevMan, Covidence, RoB/GRADE) for those. Ember hands off cleanly via its exports.

## Privacy

Everything runs locally in your browser. Your search terms and screening decisions stay on your device (browser `localStorage`). The only external calls are to the OpenAlex API; an optional email goes only to OpenAlex (for its faster "polite pool") and is stored only in your browser.

## Tech

A single `index.html` file — vanilla HTML/CSS/JavaScript, no build step, no dependencies. The animated logo is `Flame.mp4` (keep it alongside `index.html`).

## Credits

Built by **Nae** while running his own systematic review, and shared so others can do theirs faster. Data: [OpenAlex](https://openalex.org) (CC0). Screening hand-off: [ASReview](https://asreview.nl).

## License

[MIT](LICENSE) — free to use, modify, and share.
