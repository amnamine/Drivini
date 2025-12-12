# Drivini

A lightweight, static web platform that curates academic resources for students. The site aggregates well-organized links to Google Drive folders/files and highlights Computer Science Club resources, all in a clean, responsive UI with a built-in search.

## Overview
- Purpose: centralize study materials (courses, books, exams, theses) across multiple programs and levels.
- Scope: links to external resources only; no backend, accounts, or data collection.
- Language: primary UI in French; documentation in English.

## Features
- Resource catalog with quick-access buttons grouped by topic and level.
- Live search that filters visible resources as you type (`index.html:101`).
- Smooth animations on page load and while filtering.
- Responsive layout that adapts to mobile and desktop.
- Distinct gradient color themes per resource button (see `styles.css:133–169`).
- Font Awesome icons via CDN for visual consistency.

## Tech Stack
- HTML5 (`index.html`)
- CSS3 with gradients, animations, and responsive grid (`styles.css`)
- Vanilla JavaScript for search and simple animations (`index.html:100–136`)
- Assets: `drive.png` favicon
- External: Font Awesome 6 via CDN

## Repository Structure
```
.
├── index.html       # Main page and JS for search/animations
├── styles.css       # Styling, gradients, responsive rules
├── drive.png        # Favicon
└── Links.txt        # Additional resource links (reference list)
```

## Getting Started
- Prerequisites: any modern web browser and an internet connection.
- Local use: open `index.html` directly in your browser (double-click or drag into a tab).
- No build step: the project is static and has no dependencies or tooling.

## Usage
- Search: type in the search field to filter resource buttons instantly (`index.html:27`, `index.html:101`).
- Navigation: click a button to open the corresponding external resource in the same tab.
- CSCClub: access featured club resources from the dedicated section (`index.html:70–90`).

## Development
- Add a new resource button:
  1. Edit `index.html` and add a new `<button class="btn-colorX" onclick="window.location.href='URL'">Label</button>` under the `.button-container` (`index.html:30–67`).
  2. Choose an existing `btn-colorX` class (see `styles.css:133–169`) or define a new gradient class in `styles.css` following the established pattern.
- Update styles: keep to the gradient and animation conventions already present in `styles.css`.
- Icons: use Font Awesome icons by adding `<i class="fas fa-..."></i>` elements; the CDN is already included (`index.html:12`).

## Deployment
- GitHub Pages:
  - Push this repository to GitHub.
  - In repository settings, enable Pages and set source to the root of the default branch; the site will serve `index.html`.
- Vercel/Netlify:
  - Create a new project from this repo and deploy as a static site (no build command).

## Notes
- External links are maintained outside of this repository; broken links should be updated in `index.html` and `Links.txt` as needed.
- The platform does not track users or store data.

## Acknowledgements
- Computer Science Club resources showcased: `CSCC E-COPIES` and `CSCC WEBSITE`.

## License
- No license file is present. If needed, add one before public distribution.
