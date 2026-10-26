# PWA — Convert Your Website Into a Progressive Web App

A landing page for PWA_CODE: a small add-on that turns an existing website into a Progressive Web App (PWA) by adding PWA code and JavaScript files to it.

Live demo: https://pwa-setup.netlify.app/

## What it is

- **Landing page (`index.html`)** — titled "pwa_install", it pitches the idea in one screen: add the PWA code and JS files to your website and it becomes an installable Progressive Web App, with a phone mockup showing the result.
- **Service worker (`assets/js/serviceworker.js`)** — loaded by the page, it is the piece that gives a site its PWA behaviour.
- **Main script (`assets/js/main.js`)** — page scripts, loaded alongside Bootstrap/jQuery animation helpers (`assets/js/bs-animation.js`).
- **Styling and images** — Bootstrap 4, Font Awesome and Google Fonts via CDN, plus local styles in `assets/css/` (Footer-Basic, Header-Blue, Projects-Horizontal, styles) and images in `assets/img/`.

## Tech stack

- Plain HTML, CSS and JavaScript — no build step and no framework
- Bootstrap 4 and jQuery via CDN, with local CSS/JS under `assets/`
- A service worker for the PWA functionality

## How to run

There is no build step. Serve the folder with any static server and open `index.html`, for example:

```bash
npx serve .
```

or simply open `index.html` directly in a browser. The deployed version is at https://pwa-setup.netlify.app/.

## Project structure

```
index.html          # Landing page for the PWA add-on
main.html           # Additional page
assets/
  bootstrap/        # Bootstrap assets
  css/              # Footer-Basic, Header-Blue, Projects-Horizontal, styles
  fonts/            # Fonts
  img/              # Favicon and mockup images
  js/               # main.js, serviceworker.js, bs-animation.js
package.json        # Project metadata
```

## Status

A small 2022 demo/landing page. It presents the PWA add-on concept; it is not a full PWA generator — adapting it to another site means wiring its service worker and manifest into that site.
