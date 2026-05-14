# Simple Text Editor Website

This repository contains the website for [Simple Text Editor](https://simpleditor.org), a free and open-source Android app for editing plain text files.

If you are looking for the Android application source code, use [github.com/maxistar/TextPad](https://github.com/maxistar/TextPad).

## Links

- Website: [simpleditor.org](https://simpleditor.org)
- Google Play: [com.maxistar.textpad](https://play.google.com/store/apps/details?id=com.maxistar.textpad)
- F-Droid: [com.maxistar.textpad](https://f-droid.org/packages/com.maxistar.textpad/)
- Android app repository: [maxistar/TextPad](https://github.com/maxistar/TextPad)

## Technology

The website is built with [Astro](https://astro.build/) and published as a static site.

Astro is configured in [astro.config.mjs](astro.config.mjs) to write the production build to `build/`, because the GitHub Pages workflow and the legacy manual upload command both publish that directory.

## Development

Install dependencies:

```sh
npm install
```

Start the local development server:

```sh
npm run dev
```

Astro will print the local URL, usually:

```text
http://localhost:4321/
```

Build the production site:

```sh
npm run build
```

Preview the production build locally:

```sh
npm run serve
```

## Deployment

GitHub Pages deployment is handled by [.github/workflows/deploy.yml](.github/workflows/deploy.yml).

The workflow:

1. Runs on pushes to `master` or manual `workflow_dispatch`.
2. Installs dependencies with `npm ci`.
3. Builds the site with `npm run build`.
4. Uploads the generated `build/` directory as the GitHub Pages artifact.
5. Deploys it with `actions/deploy-pages`.

Manual server upload is still available:

```sh
npm run upload
```
