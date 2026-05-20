# gachewara.github.io

Personal site and portfolio for Adrian Gachewa.

Built with SvelteKit + `adapter-static`. Deploys to GitHub Pages on push to `main`.

## Develop

```bash
npm install
npm run dev
```

## Build

```bash
npm run build
```

Built site goes to `build/`.

## Deploy

Pushes to `main` trigger the GitHub Actions workflow in `.github/workflows/deploy.yml`,
which builds and deploys to GitHub Pages.

In your repo settings: **Settings → Pages → Source: GitHub Actions**.
