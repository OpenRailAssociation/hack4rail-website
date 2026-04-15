# Hack4Rail Website

Source code for [hack4rail.org](https://hack4rail.org), the website for the international hackathon for innovation in the railway sector.

## Prerequisites

- [Hugo](https://gohugo.io/) (extended version, v0.154.2+)

## Setup

Clone the repository with submodules:

```sh
git clone --recurse-submodules https://github.com/OpenRailAssociation/hack4rail-website.git
cd hack4rail-website
```

If you already cloned without submodules:

```sh
git submodule update --init --recursive
```

## Development

Run the local development server:

```sh
hugo server
```

Build the site:

```sh
hugo
```

The output is generated in the `public/` directory.

## Structure

- `content/` — Page content in Markdown
  - `challenges/` — Hackathon challenges, organized by track (`track-1/` through `track-6/`)
  - `organization/` — Participation, travel, and FAQ pages
- `config.toml` — Hugo site configuration
- `data/` — Data files (carousel, features)
- `static/img/` — Static images
- `themes/` — Hugo themes (git submodules):
  - `hack4rail` — Main site theme
  - `hugomod-images` — Image processing ([hugomods/images](https://github.com/hugomods/images))
  - `hugo-cloak-email` — Email address obfuscation ([martignoni/hugo-cloak-email](https://github.com/martignoni/hugo-cloak-email))

## Deployment

The site is built and deployed automatically via GitHub Actions on push to `main`. Pull requests generate preview deployments.

## License

CC-BY-SA 4.0 — see [LICENSE](LICENSE).
