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

```text
turf235_flashcards_site_v3/
├── index.html
├── data.json
├── README.md
└── assets/
    ├── annual-bluegrass.jpg
    ├── annual-ryegrass.jpg
    ├── bahiagrass.jpg
    ├── bermudagrass.jpg
    ├── centipedegrass.jpg
    ├── colonial-bentgrass.jpg
    ├── creeping-bentgrass.jpg
    ├── hybrid-bermudagrass.jpg
    ├── hybrid-zoysia.jpg
    ├── kentucky-bluegrass.jpg
    ├── manilagrass.jpg
    ├── mascarenegrass.jpg
    ├── perennial-ryegrass.jpg
    ├── red-fescue.jpg
    ├── redtop.jpg
    ├── rough-bluegrass.jpg
    ├── sheep-fescue.jpg
    ├── st-augustinegrass.jpg
    ├── tall-fescue.jpg
    └── velvet-bentgrass.jpg
```

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
