# McCombs Course Planner

Interactive planning dashboard for the McCombs Full-Time MBA Spring 2027 course schedule.

**Live dashboard:** published as a Claude artifact (private). The page is a single self-contained HTML file — no build step.

## Features

- All 121 Spring 2027 sections, sortable and filterable (search, department, days, Spring 1 / Spring 2 / full semester)
- Plan checkboxes with a shared, cross-device store (Claude artifact `db` capability)
- 1,000-point bid budget tracker with live over-budget warning
- Planned tab grouped by Required core / Custom core / Electives / Abroad
- "One row per course" toggle that collapses duplicate time slots
- Bid history per course: Spring 2025 average seats awarded, plus round 1 / round 2 market-clearing bids averaged across Spring 2024 and Spring 2025
- Abroad category with prior-year programs (STEP and Global Connections) kept for bid history
- RateMyProfessors rating, review count, and profile link per instructor (UT Austin, looked up Oct 2026); dashed "no RMP" chip when no profile exists

## Structure

- `index.html` — the whole app (markup, styles, data, and script in one file)

## Data notes

- 2027 sections transcribed from the MBA course schedule
- Bid stats come from the 20242 (Spring 2024) and 20252 (Spring 2025) stats sheets, averaged per course across sections within each year, then across years; a year with n/a is left out of that round's average
- Fuzzy matches worth knowing about: Envir/Social/Gov Investing → Sustainable Finance, BGS 381M → BGS 381N, STEP Mexico → Global Connections: Mexico, Behaviorl Science For Business ('24, Bryan) → Psych of Pers/Influence

## Releases

Releases are named after fruit, alphabetically.

| Release | Name | Status | Highlights |
|---|---|---|---|
| Phase 1 | **Apples** | In review ([PR #2](https://github.com/HenryDMcGee/mccombs-course-planner/pull/2)) | Medieval parchment theme: scroll rollers and unrolling parchment on load, blackletter title, ribbon tabs, wax-seal bid budget, readability-first table. Light-only rendering (dark mode removed in follow-up). Spec: [docs/specs/phase-1-parchment-theme.md](docs/specs/phase-1-parchment-theme.md) |

Pre-release foundation (unnamed): section table with sorting and filters, plan checkboxes with shared cross-device store, 1,000-point bid budget, category grouping, 2024–25 bid-history averages, RateMyProfessors ratings column.
