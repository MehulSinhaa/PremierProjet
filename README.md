# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project overview

This repository is a minimal static web page implementing a simple crowdfunding/kitty UI. It consists of a single HTML document (`index.html`) and a single stylesheet (`styles.css`). There is no JavaScript, build tooling, or backend.

`index.html` defines the structure and content of the page:
- A basic crowdfunding section with a title ("Crowdfunding / Kitty"), a goal and current amount, and a "Donate" button.
- A main page title (`<h1>`).
- A link tag that pulls in the shared stylesheet `styles.css`.

`styles.css` defines global styling rules:
- Styles for all `<h1>` elements (currently setting the text color to red).
- Styles for all `<button>` elements (font size and pointer cursor), augmenting any inline styles set directly in the HTML.

## Running and developing

There are no configured build, lint, or test commands in this repository.

To view the page during development:
- Open `index.html` directly in a web browser, or
- Serve the directory with a simple static file server, for example:
  - Using Python 3: `python -m http.server` (then open `http://localhost:8000/index.html`).

When editing styles, prefer adding or adjusting rules in `styles.css` rather than using inline styles in `index.html` so that visual changes remain centralized.

## Code structure and architecture

At a high level, the "architecture" is a straightforward separation of concerns between markup and presentation:
- **Markup (structure & content)** lives in `index.html` and is responsible for semantic elements such as headings, text, and the donation button.
- **Presentation (visual design)** lives in `styles.css`, which applies site-wide styling to headings and buttons.

There is no component system, JavaScript behavior, or build pipeline; any additional complexity (multiple pages, responsive layout, interactivity, etc.) would need to be added explicitly with new HTML, CSS, and/or JavaScript files.
