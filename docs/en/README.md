# AI Drawing Prompt Supermarket v2.7.0

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

> ⚠️ The file is large (~14MB); the first load may take several seconds. Please be patient.

- The online version is identical to the local one (same `index.html`)
- The local version still works offline (all data inlined, double-click to open)

## Compatible models

SD tag-based models: **NoobAI-XL / Illustrious / Manhwa Style / Pony Diffusion**, etc. (Danbooru tag system).

## Changelog

### v2.8.0
- **Added**: preset feature — saves one set (positive + negative). "Save preset" stores the current pos/neg prompts, "Load preset" restores and auto-rebuilds chips, "Clear preset" removes it; stored with favorites in the same `dtag_fav.json` (new format `{fav:[...], preset:{pos,neg}}`, backward-compatible import of the old array format)

### v2.7.0
- **Added**: NoobAI official tags filled in — new "Era / Date" category (old / early / mid / recent / newest date tags); "Quality" category gains `newest`, `safe`, `detailed face`, `detailed background`
- **Added**: ~44 common tags added across curated categories (character count / hairstyle / eyes / expression / body / clothing / pose / scene / style / negative); 6 new words added to the full library (chubby / bunny suit / hand on chin / fingers crossed / noise / grainy)
- **Fixed**: clicking a prompt chip's body no longer toggles positive/negative (only the `±` button toggles; left-click is for drag-reorder only)
- **Optimized**: added a structure navigation + maintenance guide comment at the top of the file, marking the huge full-library line so AIs can read/maintain it safely

### v2.6.0
- **Added**: prompt weight recognition — pasting `(tag:weight)` auto-recognizes the tag and shows a weight badge; group weights `(a, b:1.5)` apply to every tag in the group; weight 1 is not shown (equivalent to no weight)
- **Added**: right-click a chip to adjust weight — popup with manual input (arabic numerals only, default 1) + `±0.1` step buttons + a reset button (reset to 1)
- Unmatched weighted tags are kept verbatim (e.g., `(weird thing:1.3)` is preserved as-is)

### v2.5.0
- **Added**: `×` delete button on prompt chips; `±` moved to the leftmost side of chips (toggles positive/negative), turns red only on hover and only the one under the cursor, with a pointer cursor
- **Added**: auto-save folder path shown to the right of the button (`folder name / dtag_fav.json`), aligned on the same line as the button text
- **Added**: right-click reselect now starts from the last used folder (`startIn`)

### v2.4.1
- **Fixed**: the search results list no longer disappears when clicking other buttons while the search box still has text (it only hides when the box is cleared or a result is selected)

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
