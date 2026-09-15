# Tasks

A retro VHS-styled task manager (Today / Weekly / Dashboard views, folders, subtasks, drag-and-drop) built as an installable PWA.

## Local preview
Just open `index.html` in a browser. Note: some features (like persistent storage) only work when served over http(s), not `file://` — use a local server, e.g.:

```
npx serve .
```

## Deploying
This is a static site — any static host works (GitHub Pages, Netlify, Vercel, Firebase Hosting).

### GitHub Pages
1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under "Build and deployment", set **Source: Deploy from a branch**, branch: `main`, folder: `/ (root)`.
4. Your app will be live at `https://<username>.github.io/<repo>/`.

## Turning it into an Android app
Once hosted, this manifest + service worker make the site installable as a PWA directly from Chrome ("Add to Home screen").

To get a real installable `.apk`, use [Bubblewrap](https://github.com/GoogleChromeLabs/bubblewrap):

```
npm install -g @bubblewrap/cli
bubblewrap init --manifest=https://your-hosted-url/manifest.json
bubblewrap build
```
