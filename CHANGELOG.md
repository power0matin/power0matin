# Changelog

All notable changes to this repository are documented here.

## [3.1.0] - 2026-07-12

Migrate from deprecated github-readme-stats to actively maintained GitHub Stats Extended.

### Changed

- **All GitHub Stats URLs** — migrated 8 endpoints from `github-readme-stats.vercel.app` to `github-stats-extended.vercel.app`
- **6 repository pin cards** — now served by GitHub Stats Extended
- **GitHub Stats card** — migrated to new API
- **Top Languages card** — migrated to new API

### Compatibility

- GitHub Stats Extended is fully compatible with github-readme-stats parameters
- No parameter changes required — `theme`, `hide_border`, `show_icons`, `count_private`, `include_all_commits`, `rank_icon`, `layout`, `langs_count` all supported
- `streak-stats.demolab.com` remains unchanged (actively maintained, v1.7.0)

### Migration Notes

- Old `github-readme-stats.vercel.app` public deployment is paused/deprecated
- `github-stats-extended.vercel.app` is the actively maintained successor (303 stars, 115 forks, v2.1.3)
- All existing themes (tokyonight) are supported
- All existing API parameters are compatible

## [3.0.0] - 2026-07-12

Production release — full repository audit, community health files, and final polish.

### Added

- **`.gitignore`** — covers OS artifacts, editor files, dependencies, and environment files
- **`.editorconfig`** — enforces consistent formatting across editors (LF line endings, UTF-8, trailing whitespace rules)
- **`.markdownlint.json`** — disables line length, inline HTML, and first-line-heading rules for profile README compatibility
- **`.github/FUNDING.yml`** — enables GitHub sponsor button linking to CoffeeBede
- **`.github/ISSUE_TEMPLATE/bug_report.md`** — structured template for reporting broken links or issues
- **`.github/ISSUE_TEMPLATE/config.yml`** — disables blank issues, provides email as alternative contact
- **`.github/PULL_REQUEST_TEMPLATE.md`** — checklist for validating link, markdown, and accessibility

### Changed

- **Banner image** — moved from repo root to `assets/github-header-image.png` for cleaner structure
- **README banner path** — updated to relative path `assets/github-header-image.png`
- **Analytics section** — removed unnecessary `<br />` between stats and streak
- **CHANGELOG scope** — expanded from "profile README" to "this repository" to reflect broader maintenance

### Removed

- **`<br />` in GitHub Analytics** — unnecessary line break; centering div provides adequate spacing

## [2.1.0] - 2026-07-12

Professional refinement pass — tightened content, updated repos, removed visual noise.

### Added

- **linux-network-optimizer** — replaced discord-quest-auto-completer in Featured Projects
- **FastAPI, PostgreSQL, JavaScript, GitHub Actions, Linux** — added to Tech Stack (represent current active stack)
- **Support badge** — switched to `flat-square` for consistency with all other badges

### Changed

- **Header tagline** — changed from "Python & Django · Automation & Tooling" to "Linux & DevOps · Automation & Open Source" to reflect current identity
- **About section** — rewrote to 5 focused lines covering Backend Engineering, Python, Linux, DevOps, Automation, Open Source; removed narrative tone
- **Currently Working On** — condensed to one-line-per-project format with no descriptions
- **Featured Projects** — replaced discord-quest-auto-completer with linux-network-optimizer; now features 6 repos representing current expertise
- **Tech Stack** — expanded to 12 technologies from 10; added FastAPI, PostgreSQL, JavaScript, GitHub Actions, Linux; removed Lua, C#, GitHub (separate icon)
- **Tech Stack layout** — flattened into a single centered row of icons with no sub-headings; fastest possible scan
- **GitHub Analytics** — removed trophy section entirely; kept Stats, Top Languages, and Streak in a cleaner layout
- **Open Source Focus** — rewrote to five focused areas: Linux tooling, Backend engineering, DevOps automation, Networking, CLI utilities
- **Development Philosophy** — replaced verbose principles with five concise one-liners
- **Support section** — collapsed description text into single line with footer message

### Removed

- **GitHub Trophies** — decorative noise, no meaningful signal
- **Lua and C#** from Tech Stack — no longer representative of current work
- **GitHub as separate icon** — redundant with GitHub Actions; GitHub profile link in Connect section covers it
- **"Currently strengthening" paragraph** from About — unnecessary filler
- **Verbose project descriptions** from Currently Working On — titles alone are sufficient
- **"If any of my projects helped you"** intro from Support — the badge speaks for itself

### Metrics

- **162 lines** (down from 184 in v2.0.0, down from 382 original)
- **Zero** horizontal rules
- **Zero** trophy references
- **12** tech stack icons (all actively used)
- **6** featured project cards (all current)

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
