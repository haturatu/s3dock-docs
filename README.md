# S3Dock Docs

This is the public GitHub Pages site for S3Dock.

The site is built with Hugo and is intended to be managed as a separate public repository named `s3dock-docs`.

## Local Development

```bash
hugo server
```

Open the local URL printed by Hugo.

## Production Build

```bash
hugo --minify
```

The generated site is written to `public/`.

## GitHub Pages

1. Push this directory to a public GitHub repository named `s3dock-docs`.
2. In the repository settings, enable GitHub Pages with **Source: GitHub Actions**.
3. Push to the `main` branch.
4. The workflow in `.github/workflows/deploy.yml` builds and deploys the site.

Default Pages URL:

```text
https://haturatu.github.io/s3dock-docs/
```

If the repository owner or name changes, update `baseURL` in `hugo.toml`.
