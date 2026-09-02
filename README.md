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

The site is organized by course module, matching the TURF 235 Canvas module list. `public_html/index.html` just redirects to `turf235/index.html`, which links out to each module. Only Module 2 has real content so far; the others are outline stubs (topic list only) reserving the structure.

```text
public_html/
├── index.html                     redirects to turf235/index.html
└── turf235/
    ├── index.html                 module list for the course
    ├── module1/                   Module 1: A Campus Walk (outline only)
    │   ├── index.html             topic outline / study guide
    │   ├── flashcards.html        placeholder
    │   └── text-quiz.html         placeholder
    ├── module2/                   Module 2: Up Close and Personal (active)
    │   ├── index.html             browsable trait reference for all 20 species
    │   ├── flashcards.html        picture-based multiple choice quiz
    │   ├── text-quiz.html         fill-in-the-dropdowns vegetative traits quiz
    │   ├── data.json
    │   ├── README.txt
    │   └── assets/                species photos
    ├── module3/                   Module 3: Watching Grass Grow: Vegetatively (outline only)
    │   ├── index.html
    │   ├── flashcards.html
    │   └── text-quiz.html
    └── module4/                   Module 4: Watching Grass Grow: Reproductively (outline only)
        ├── index.html
        ├── flashcards.html
        └── text-quiz.html
```

Each module folder's `index.html` is its study guide, with `flashcards.html` and `text-quiz.html` alongside it. Fill in a placeholder module by replacing those three files.

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
