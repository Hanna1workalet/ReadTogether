# ReadTogether

A reading website where readers talk about a book page by page. Notes are attached to the page they belong to, so you only see them when you reach that page and never before.

> **Status:** front-end prototype. All four pages are static HTML and CSS with sample data. Accounts, saving notes and real books are not built yet (see [Roadmap](#roadmap)).

## Features (current design)

| Feature | Page |
|---|---|
| Currently reading card, personal shelf, community reads | Home |
| Book details, genres, rating, reader count, personal progress | Book |
| Reading view with per-page notes and a note form | Reading |
| Reader stats, recently finished books, activity trail | Profile |
| Skip link, labelled navigation, semantic HTML | All pages |
| Responsive layout (desktop, tablet, phone) | All pages |

## Pages

| File | Purpose |
|---|---|
| `index.html` | Home: reading room, current read, shelf, community reads |
| `book.html` | Details for one book and a preview of its conversations |
| `reading.html` | Chapter text, notes for the current page, previous/next page |
| `profile.html` | Reader profile, stats and recent activity |

## Project structure

```
ReadTogether/
├── index.html
├── book.html
├── reading.html
├── profile.html
├── css/
│   ├── base.css       # tokens, reset, header, buttons, cards, progress bar
│   ├── home.css
│   ├── book.css
│   ├── reading.css
│   └── profile.css
├── images/
├── README.md
└── LICENSE
```

Each page has its own stylesheet, and every page stylesheet starts with `@import url("base.css");` so shared styles load first.

## Design system

Colors, fonts, radius and shadow are CSS variables defined in `:root` in `css/base.css`.

| Token | Use |
|---|---|
| `--paper`, `--ivory`, `--beige` | Backgrounds |
| `--charcoal` | Main text |
| `--muted` | Secondary text |
| `--purple`, `--purple-dark`, `--dark`, `--purple-soft` | Brand colors and accents |
| `--line` | Borders |
| `--card` | Card background gradient |
| `--radius`, `--shadow` | Card shape and depth |
| `--header-h` | Header height |

Fonts are loaded from Google Fonts in the `<head>` of every page. The font names in the `<link>` tag must match the names in `base.css`.

## Run locally

No build step or dependencies.

1. Download or clone the project.
2. Open `index.html` in a browser, or use the VS Code **Live Server** extension for auto-reload.
3. Use the navigation to visit the other pages.

The entry file must be named `index.html`.

## Roadmap

- [x] Home, book, reading and profile pages
- [ ] Shared styles consistent across all pages
- [ ] JavaScript: page navigation, progress, search, note form
- [ ] Backend and accounts (for example Supabase or Firebase) so notes persist
- [ ] Real book content split into pages (start with public-domain books)
- [ ] Likes and replies on notes
- [ ] Moderation and reporting
- [ ] Privacy policy and terms of use

## Notes

- Names, books, counts and notes on every page are placeholder content.
- The note form and the "Save to my Books" button do not save anything yet.

## Accessibility

- Skip link on every page
- `aria-label` on navigation, search and avatar links
- Native `<progress>` elements for reading progress
- Keyboard-reachable buttons and links

## License

See [LICENSE](LICENSE).
