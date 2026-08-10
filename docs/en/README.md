# AI Drawing Prompt Supermarket v2.4.0

[**中文简体**](../../README.md) | **English**

A local, offline AI drawing prompt generator: **click Chinese tags to auto-generate English prompts**. Single-file, zero-dependency, double-click to run.

## Features

- **Full tag library**: 320K+ Danbooru Chinese–English tag pairs (characters / artists / copyrights / works), daily-updated data source
- **Categories + subcategories**: hair color / hairstyle / eyes / expression / body / clothing / pose / scene / style / NSFW, with deep subcategories (e.g. clothing → tops / dresses / underwear / shoes & accessories)
- **Global search**: search by Chinese, English, underscores, or spaces across the full library
- **Favorites**: ★ favorite common tags, filter by "favorites only", persisted across sessions; **favorite directly from search results with ☆**
- **Import / Export favorites**: export favorites to a JSON file for backup, or import & merge from a JSON file; export is alphabetically sorted for clean diffs
- **Auto-save**: when enabled, favorites auto-write to a chosen JSON file on every change (built-in memory is kept; the file is a parallel backup). Requires Chrome/Edge — pick the location once on first enable, right-click the button to re-pick anytime
- **Browse all**: view the 1000 most-used tags in one click
- **Negative prompts**: built-in negative categories, auto-routed to the negative box
- Underscores auto-convert to spaces on output (`long_hair` → `long hair`), ready to paste into workflows
- **Drag to reorder**: drag the Chinese chips below the prompt bar to change prompt order
- **Prompt backfill recognition**: paste or type an existing prompt into the positive/negative boxes to auto-convert into chips (matched tags show Chinese; unmatched keep the original text with a `?` marker)

## Usage

Open `index.html`, click Chinese tags in the categories, and the prompt bar at the top assembles English prompts for one-click positive / negative copy.

## Online (GitHub Pages)

Hosted on GitHub Pages, use it online without downloading:

**https://bfrkqsb7.github.io/ai-prompt-supermarket/**

- The online version is identical to the local one (same `index.html`)
- The local version still works offline (all data inlined, double-click to open)

## Compatible models

SD tag-based models: **NoobAI-XL / Illustrious / Manhwa Style / Pony Diffusion**, etc. (Danbooru tag system).

## Changelog

### v2.4.0
- **Added**: prompt backfill recognition — paste or type an existing prompt into the positive/negative boxes to auto-convert into chips (matched tags show Chinese; unmatched keep the original text with a `?` marker)
- **Removed**: dropped the `index_old.html` old-version backup (git history serves as the backup; no longer shipped with the repo)

### v2.3.0
- **Added**: drag the Chinese chips below the prompt bar to reorder prompts
- **Version**: page title changed to "AI Drawing Prompt Supermarket v2.3.0"

### v2.2.0
- **Added**: favorite/unfavorite tags directly from search results with ☆

### v2.1.0
- **Added**: Import favorites from a JSON file (merge)
- **Added**: Export favorites to a JSON file (alphabetically sorted)
- **Added**: Auto-save favorites to a chosen JSON file on change (requires Chrome/Edge; re-pick location anytime)
- **Fixed**: Missing Chinese labels for some favorited tags (tags only in curated categories but not in the full library showed English)
- **Version**: previous version backed up as `index_old.html`

## Notes

- Single-file HTML, all data inlined, works offline, ~14MB
- The tag library covers adult-content categories; please comply with local laws and platform policies, and do not generate content involving minors
