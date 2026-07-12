# Changelog

All notable changes to the GitHub profile README are documented here.

## [2.0.0] - 2026-07-12

Complete redesign of the GitHub profile README for a modern, premium look.

### Added

- **"Currently Working On" section** — highlights active projects so visitors immediately see what's in progress
- **"Open Source Focus" section** — communicates the types of open-source work being done
- **"Development Philosophy" section** — five concise principles that define the approach to software
- **GitHub stats cards as project pins** — replaced static badge-heavy project cards with dynamic `github-readme-stats` pinned repo cards (auto-update with stars, language, forks)
- **GitHub icon in Connect section** — added a direct GitHub profile link alongside social links
- **Docker to Tech Stack** — added Docker icon since it's relevant to backend/deployment work

### Changed

- **Header** — replaced multi-line role description with single-line bold tagline for cleaner visual hierarchy
- **Badge row** — switched from `for-the-badge` style to `flat-square` for a more compact, modern look; removed redundant profile view count from badge text
- **About section** — rewrote from verbose bullet-list format to two concise paragraphs; removed the Persian name transliteration (still present in GitHub profile itself)
- **Tech Stack** — replaced three separate `<table>` layouts with single-line inline icon rows; reduced from 120px wide table cells to simple icon image tags
- **Featured Projects** — replaced 6-cell table layout with 6 pinned repo cards using `github-readme-stats` API; removed inline language/framework badges per card
- **GitHub Analytics** — added `&nbsp;` spacing between Stats and Top Languages cards to reduce vertical whitespace; tightened trophy margin settings
- **Connect section** — replaced `<table>` layout with inline icon links using `&nbsp;` spacing; standardized all icons to 40px width; added consistent `aria-label` attributes
- **Support section** — replaced raw CoffeeBede SVG banner with a shields.io badge button for visual consistency
- **Footer** — simplified closing text and removed `<br />` padding

### Removed

- **Progress bars ("Current Focus")** — ASCII progress bars are not meaningful, not accessible, and add visual clutter; replaced by the more informative "Currently Working On" section
- **Three separate Tech Stack tables** — replaced with inline icon rows that take 70% less vertical space
- **Project description tables with inline badges** — each project had its own description + 2-3 badges; replaced with auto-updating pinned repo cards
- **Duplicate Contact section** — the old README had both a "Connect With Me" social table AND a separate "Contact" section with email/LinkedIn badges; merged into a single "Connect" section
- **"Thanks for visiting" heading** — removed as unnecessary; the footer message covers the same sentiment
- **Excessive `<br />` tags** — removed 12+ explicit line breaks that were inflating vertical spacing
- **"Revise" and "Delete" commit-style comments** — cleaned up all unnecessary HTML comments
- **`for-the-badge` badge style** — replaced everywhere with `flat-square` or removed entirely

### Design Decisions

1. **No horizontal rules (`---`)** — used heading hierarchy and whitespace for section separation instead, following modern profile README conventions
2. **Pinned repo cards over custom tables** — `github-readme-stats` pin cards are dynamic (update with stars/forks/language) and maintain consistent styling without manual upkeep
3. **`tokyonight` theme consistency** — all GitHub stats images use the same theme for visual cohesion
4. **Flat-square badges** — cleaner and less visually heavy than `for-the-badge` style
5. **Inline icons over table layouts** — tech stack icons in a single row reduce vertical space from ~150px to ~60px per category
6. **`aria-label` on all links** — ensures accessibility for screen readers
7. **184 lines total** — well under the 350-line target; every line earns its place
