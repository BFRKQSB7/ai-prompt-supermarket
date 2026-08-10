# AI Drawing Prompt Supermarket v2.1.0

[**中文简体**](../../README.md) | **English**

A local, offline AI drawing prompt generator: **click Chinese tags to auto-generate English prompts**. Single-file, zero-dependency, double-click to run.

## Features

- **Full tag library**: 320K+ Danbooru Chinese–English tag pairs (characters / artists / copyrights / works), daily-updated data source
- **Categories + subcategories**: hair color / hairstyle / eyes / expression / body / clothing / pose / scene / style / NSFW, with deep subcategories (e.g. clothing → tops / dresses / underwear / shoes & accessories)
- **Global search**: search by Chinese, English, underscores, or spaces across the full library
- **Favorites**: ★ favorite common tags, filter by "favorites only", persisted across sessions
- **Import / Export favorites**: export favorites to a JSON file for backup, or import & merge from a JSON file; export is alphabetically sorted for clean diffs
- **Auto-save**: when enabled, favorites auto-write to a chosen JSON file on every change (built-in memory is kept; the file is a parallel backup). Requires Chrome/Edge — pick the location once on first enable, right-click the button to re-pick anytime
- **Browse all**: view the 1000 most-used tags in one click
- **Negative prompts**: built-in negative categories, auto-routed to the negative box
- Underscores auto-convert to spaces on output (`long_hair` → `long hair`), ready to paste into workflows

## Usage

Open `index.html`, click Chinese tags in the categories, and the prompt bar at the top assembles English prompts for one-click positive / negative copy.

## Online (GitHub Pages)

Hosted on GitHub Pages, use it online without downloading:

**https://bfrkqsb7.github.io/ai-prompt-supermarket/**

- The online version is identical to the local one (same `index.html`)
- The local version still works offline (all data inlined, double-click to open)
- `index_old.html` is the previous version backup; it doesn't affect usage

## Compatible models

SD tag-based models: **NoobAI-XL / Illustrious / Manhwa Style / Pony Diffusion**, etc. (Danbooru tag system).

## Changelog

### v2.1.0
- **Added**: Import favorites from a JSON file (merge)
- **Added**: Export favorites to a JSON file (alphabetically sorted)
- **Added**: Auto-save favorites to a chosen JSON file on change (requires Chrome/Edge; re-pick location anytime)
- **Version**: previous version backed up as `index_old.html`

## Notes

- Single-file HTML, all data inlined, works offline, ~14MB
- The tag library covers adult-content categories; please comply with local laws and platform policies, and do not generate content involving minors
