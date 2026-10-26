# Matcha Melbourne

A Vietnamese-language matcha directory for Melbourne, built with static HTML, CSS and JavaScript. No build, API key or backend is needed.

## What works

- Ten locations across Melbourne CBD, Carlton, South Yarra, Southbank and Clayton.
- Search by café, suburb, address or menu item, including Vietnamese without accents and multiple keywords.
- Combined category, suburb, reference-drink price and saved-only filters; price and name sorting. Unknown prices sort last.
- Dedicated café profiles, selected menu items, source links, address, published hours and price caveats.
- Google Maps for a selected address, direct directions and a CBD walking route.
- Saved cafés, private tasting notes and a local café-suggestion notebook with JSON export.
- Responsive layouts, local fonts, SVG icons, keyboard search shortcut, labelled controls, focus states and reduced-motion support.

## Data and its limits

Sources were checked on 26 October 2026. There are eight brands and ten locations. Six locations have a sourced reference-drink price, four do not. Official websites/menus and City of Melbourne supply addresses and selected menu items. Little Rogue prices are from a third-party menu index and are explicitly labelled. itteki South Yarra uses a seasonal menu and is labelled accordingly. Hareruya branch prices come from the shared brand website, not separate in-store verification.

Displayed prices are AUD reference prices, not guaranteed current checkout prices. Each profile gives its exact source and caveats. Additional milk, size, toppings and holiday surcharges may apply. Price filters use the named reference drink, not the cheapest menu item or add-on. Unknown prices stay unknown. Menus are selections, not complete reproduced menus. No ratings or review counts are fabricated.

Imagery is AI-generated editorial illustration, explicitly labelled. It is not photography of named businesses or their actual menu items. See `ASSETS.md` for provenance.

Saved cafés, tasting notes and suggestions stay in browser localStorage; there is no account, shared database, editorial inbox, public review system, analytics or automatic data refresh. Data keys from the earlier version are preserved. Google Maps is embedded on the area page; other outbound venue links open only when selected.

## Files

- `dist/index.html`: directory entry page.
- `dist/cafe-spotlight.html`: café detail page (`?cafe=little-rogue`, etc.).
- `dist/matcha-map-and-suburbs.html`: address map and area search.
- `dist/community-and-submit.html`: local notebook and FAQs.
- `dist/assets/app.js`: rendering, filters and local persistence.
- `dist/assets/data.js`: browser café data.
- `data/cafes.json`: editable data source with venue-specific evidence links.
- `dist/assets/site.css`: responsive styling.
- `dist/assets/fonts.css` and bundled font files: Hanken Grotesk and Newsreader, including Vietnamese subsets.
- `.openai/hosting.json`: existing Sites identity and static directory.

When changing café data, update both JSON and `data.js` (or regenerate the latter as `window.MATCHA_CAFES = <JSON>;`). Verify the exact branch and menu source before changing prices.

## Run locally

```sh
python3 -m http.server 3000 --directory dist
```

Open http://localhost:3000. Any static host can serve `dist/`. Existing assets from the earlier design remain in the source history and checkout.

## Validation

JavaScript syntax checks, data/source consistency checks and browser checks cover accent-insensitive search, combined filters, unknown-price sorting, empty states, persistence, detail menu tabs, local notes, map selection and notebook validation. Desktop browser QA is recorded in `VALIDATION.md`; responsive breakpoints are implemented in CSS.

## Hosting

The associated Sites project preserves its owner-private audience. The GitHub repository stores source; the repository name alone does not configure the `matchamelbourne.com` custom domain. Deployments require the Sites workflow, or a separately configured static host.
