# link:up website

The website for the link:up event

Currently reachable on [https://marrold.github.io/linkup-website](https://marrold.github.io/linkup-website)

## Requirements

- Python 3.10 or newer
- MkDocs and the Material for MkDocs theme - see [requirements.txt](requirements.txt)

## Installing

Using a virtual environment keeps the packages separate from the rest of the system:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Developing locally

Start the development server:

```bash
mkdocs serve
```

The site is then available at http://127.0.0.1:8000 and reloads when a file is saved.

To check the site the same way the deployment does, run a strict build. It fails on warnings such as broken links:

```bash
mkdocs build --strict
```

The output goes to the `site/` directory, which is not committed.

## Layout

- `docs/` holds the pages, images and custom CSS
- `overrides/` holds theme template overrides, such as the announcement bar
- `mkdocs.yml` holds the site configuration and navigation

## Publishing

Pushing to `main` builds the site and publishes it to GitHub Pages using the workflow in `.github/workflows/pages.yml`. It can also be run by hand from the Actions tab on GitHub.
