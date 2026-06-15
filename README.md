# go-fde.github.io

Sources for **go-fde.github.io** — the go-fde landing page.
Built with [Hugo](https://gohugo.io), using the same single-template,
inline-CSS shape as the other sibling org landings.

## Layout

```text
.
├── hugo.toml                 Site config + repo card params
├── content/
│   └── _index.md             Homepage marker (empty)
├── layouts/
│   └── index.html            Homepage body (single template, inline CSS)
├── static/
│   ├── favicon.svg           Favicon (the go-fde mark)
│   └── img/logo.svg          Hero logo (the go-fde mark)
└── public/                   Hugo build output (gitignored — built by CI)
```

## Build locally

```sh
hugo server -D                 # live reload at http://localhost:1313/
hugo --gc --minify             # production build → ./public/
```

## Deploy

`.github/workflows/hugo.yml` builds and deploys on every push to `main`.
Configure GitHub Pages with **Source = "GitHub Actions"** (not "Deploy
from a branch").
