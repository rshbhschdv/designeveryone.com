# designeveryone.com

A Hugo site that serves the imported `designeveryone` website design.

## What was converted

The original design package was a Vite/React single-page app. It has been converted into this Hugo project by:

- building the original app once
- copying the compiled JavaScript bundle into `static/assets/designeveryone-app.js`
- copying the favicon into `static/favicon.svg`
- replacing the Hugo homepage template with a minimal shell that mounts the app

## Run locally

Run Hugo:

```bash
hugo server -D
```

The imported site will be available through Hugo at `http://localhost:1313`.

## Build for production

```bash
hugo
```

The generated site will be written to `public/`.

## Important files

- `layouts/index.html`: Hugo homepage shell for the imported app
- `static/assets/designeveryone-app.js`: compiled application bundle
- `static/favicon.svg`: site favicon
- `.tmp-convert/designeveryone/`: extracted original package used during conversion

## Updating the design later

If the original React design changes, rebuild it inside `.tmp-convert/designeveryone/` and copy the new build output into `static/`.
