# Antoine Royer Bournelle — Portfolio

Bilingual (EN/FR) static portfolio for a data engineer, built as a single-page site with no build step.

**Live site:** <https://antoineroyerb.github.io/>

## Features

- Hero, Experience, Projects, Skills, Education, and Contact sections
- EN/FR language toggle (client-side i18n, no page reload)
- Downloadable CV (`assets/docs/CV.pdf`)
- Responsive layout, light/dark aware

## Stack

Plain HTML5, CSS3, and vanilla JavaScript — no framework, no bundler. The i18n
dictionary and language-switching logic live inline in `index.html`; content
strings are swapped via `data-i18n` attributes.

## Structure

```
index.html          Page markup + inline i18n script
css/styles.css       Styles
assets/img/          Profile image
assets/docs/CV.pdf    Downloadable resume
robots.txt, sitemap.xml  SEO
```

## Local preview

No build step required — open `index.html` directly in a browser, or serve it:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deployment

Served via GitHub Pages from the `main` branch — pushing to `main` publishes
the live site automatically.

## Updating content

- **Text (EN/FR):** edit the `i18n` dictionary in the `<script>` block near
  the end of `index.html`, and the matching `data-i18n` attributes in the
  markup.
- **CV:** replace `assets/docs/CV.pdf`.
