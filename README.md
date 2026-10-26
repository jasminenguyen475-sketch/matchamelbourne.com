# Matcha Melbourne

A responsive matcha café directory built from the four supplied page designs. The website is static HTML, CSS and JavaScript; it does not need a framework, API key or production build step.

## Preview locally

```sh
python3 -m http.server 3000 --directory dist
```

Open `http://localhost:3000`.

## Pages and behaviour

- **Explore & Directory:** six sample cafés, text search, combined suburb/price/intensity/dietary filters, empty states, and bookmarks.
- **Café Spotlight:** the full Hareruya Pantry design and an individual detail view for each directory café. Menu category tabs, sharing, directions and personal tasting notes work.
- **Map & Suburbs:** an explicitly illustrated map with selectable cafés, suburb filters, zoom controls, and two walking crawls that open Google Maps directions.
- **Community & Submit:** validated café suggestions, up to three photo thumbnails, a local suggestion log, JSON export and explanatory FAQs.
- **Shared:** responsive navigation, global café search, keyboard shortcut, saved list, labelled controls, focus indicators and reduced-motion support.

## Data and storage

Venue names, menu items, prices, ratings, hours, imagery and descriptions originate from the supplied design and remain **sample content**. They have not been independently verified. Visible preview notices explain this.

Saved cafés, tasting notes and café suggestions use this browser’s local storage. They do not sync between devices or reach an editorial team. Clearing site data removes them. The suggestion download includes saved photo thumbnails. There is no account system, email delivery, public review backend or analytics service.

## Edit the website

- `dist/*.html`: the four page layouts and editorial copy.
- `dist/assets/data.js`: the six café profiles used by search, maps and detail views.
- `dist/assets/app.js`: browser interactions and local persistence.
- `dist/assets/site.css`: shared styling, mobile layouts and component styles.
- `dist/assets/tailwind.css`: compiled utility styles.
- `dist/assets/`: bundled design images, local fonts, favicon and font licences.

All rendered assets are served locally. Google Maps and Instagram links open external services only when selected.

If you add new Tailwind utility classes to the HTML or JavaScript, regenerate the utility stylesheet from the project root:

```sh
npx --yes tailwindcss@3.4.17 -i ./input.css -o ./dist/assets/tailwind.css -c ./tailwind.config.cjs --minify
```

## Hosting

Upload the contents of `dist/` to a static web host. Paths are relative, so the site also works below a repository path. The tracked `.openai/hosting.json` retains the associated Sites project identity.

The repository name `matchamelbourne.com` does not itself configure that custom domain. Domain configuration and a shared submission/review backend can be added separately.
