# TURF 235 Turfgrass ID Quiz

A lightweight, static study website for practicing turfgrass identification for **Penn State TURF 235**.

The site uses flashcard-style visuals and multiple-choice questions to help reinforce species identification by morphology.

## Features

- Multiple-choice turfgrass identification
- 20 turfgrass species
- Local image assets
- Filter by turfgrass group
- Filter by vernation:
  - Folded
  - Rolled
- Shuffle the active deck
- Correct answers are removed from the deck
- Incorrect answers are moved to the back of the deck and shown again later
- No automatic advance after answering
- **Proceed** button lets you review the answer before moving on
- Previous and Skip / Next controls
- Keyboard shortcuts
- Responsive layout for desktop, tablet, and mobile
- No database or server-side code required

## Study Logic

The quiz is designed to behave like a simple repetition system.

### Correct Answer

When you answer correctly:

1. The correct choice is highlighted.
2. The species is removed from the active deck.
3. The quiz waits for you to click **Proceed**.

### Incorrect Answer

When you answer incorrectly:

1. Your selected answer is marked incorrect.
2. The correct answer is highlighted.
3. The species is moved to the back of the active deck.
4. It will appear again later.
5. The quiz waits for you to click **Proceed**.

The deck is complete when every active species has been answered correctly.

## Filters

### Turfgrass Group

You can limit the deck to:

- Bluegrass
- Bentgrass
- Ryegrass / Fescue
- Bermuda
- Zoysia
- Broad-blade warm-season grasses

### Vernation

You can also filter by:

- Folded
- Rolled

Both filters can be used together.

For example:

```text
Ryegrass / Fescue + Folded
```

will show only species matching both conditions.

## Keyboard Shortcuts

| Key | Action |
|---|---|
| `1`–`4` | Choose an answer |
| `Enter` | Proceed after answering |
| `←` | Previous card |
| `→` | Skip / Next card |

## Files

The site is organized as a landing page linking out to per-course modules. Only the TURF 235 module has real content so far; the rest are placeholders reserving the structure.

```text
public_html/
├── index.html                     landing page, links to every module
└── modules/
    ├── turf235/                   TURF 235 — The Turfgrass (active)
    │   ├── flashcards.html        picture-based multiple choice quiz
    │   ├── study-guide.html       browsable trait reference for all 20 species
    │   ├── text-quiz.html         fill-in-the-dropdowns vegetative traits quiz
    │   ├── data.json
    │   ├── README.txt
    │   └── assets/                species photos
    ├── turf230/                   TURF 230 — Turfgrass Pesticides (placeholder)
    ├── turf238-307/               TURF 238/307 — Weed Control & Golf Course Irrigation (placeholder)
    ├── turf434/                   TURF 434 — Turfgrass Edaphology (placeholder)
    ├── turf435/                   TURF 435 — Turfgrass Nutrition (placeholder)
    └── turf436w/                  TURF 436W — Case Studies in Turfgrass Management (placeholder)
```

Each module folder holds a `study-guide.html` and a `text-quiz.html`. Add real content to a placeholder module by replacing those two files.

## Hosting

This is a fully static website.

Upload the entire directory to your web server and open:

```text
index.html
```

No build process is required.

It should work on standard static hosting such as:

- Apache
- Nginx
- GitHub Pages
- Netlify
- Any basic shared web host

## Notes

The site is intended as a study aid for turfgrass identification. The current deck includes visual and morphological characteristics used in TURF 235 study materials, including vernation and species-level identification traits.

If you update any card images or species data, keep the filenames referenced in `data.json` synchronized with the files in the `assets/` directory.
