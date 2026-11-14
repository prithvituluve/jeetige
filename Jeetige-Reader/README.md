# Jeetigè Digital Book Reader

Complete source for the mobile-ready website. No build step or API keys required.

## Run locally

1. Extract the ZIP.
2. Open a terminal in the Jeetige-Reader folder.
3. Run `python -m http.server 8000` (Windows) or `python3 -m http.server 8000` (macOS/Linux).
4. Open http://localhost:8000 in a modern browser.

Use a local web server; opening index.html directly through file:// will not load the PDFs and JavaScript modules correctly. VS Code Live Server also works.

## Files

- index.html — page structure and controls
- style.css — book appearance and responsive layouts
- app.js — PDF rendering, page flips, zoom and reading progress
- assets/book.pdf — original 48-page interior PDF
- assets/cover.pdf — original four-page cover PDF
- assets/cover.png — front-cover preview
- vendor/ — PDF.js 4.10.38 and StPageFlip 2.0.7, included locally

## Hosting

Upload the folder contents to a static web host. Keep the folders and file names intact. The hosting root must contain index.html. There is no build command. Serve .mjs files as JavaScript and .pdf files as application/pdf. HTTPS is recommended for fullscreen and browser compatibility.

## Reading

Desktop uses a two-page spread. Small screens and touch devices use one page. Swipe or tap page corners, or use the navigation controls. When zoomed in, scroll to pan and use the arrow buttons to change pages. Reading progress is kept in sessionStorage for the current browser session.

## Content and customization

Edit the HTML and CSS to change the title, colours and layout. PDF page mapping currently targets this particular book: cover pages 1–2, all 48 interior pages, then cover pages 3–4. If replacing the book with one having a different page count, update the mapping and related limits in app.js and index.html.

The PDF artwork and text retain their original rights. Third-party libraries retain their respective licenses; see vendor/LICENSE files. Hosting account configuration, credentials and Git history are not part of this portable export.
