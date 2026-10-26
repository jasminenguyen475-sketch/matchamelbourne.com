# Validation — 26 October 2026

Passed:

- Node syntax checks for `app.js` and `data.js`.
- Ten unique café IDs, five suburbs, six labelled price references and four explicitly unknown references.
- JSON and browser data copies match; every venue has dated evidence links and price caveats.
- Local HTML links, bundled CSS/font/image references and static element IDs checked.
- Desktop browser rendered directory and café detail pages with local fonts, native SVG icons and illustrative photos.
- Search `nguyen chat` returned Little Rogue, Matcha Kōbō and Chayō, proving Vietnamese accent folding.
- Melbourne CBD + under A$8 returned Little Rogue and Hareruya Pantry CBD.
- Ascending price order began with Chayō; four unknown-priced locations remained at the end.
- Saving Little Rogue, saved-only filtering and reload preserved the selection. Unsaving produced the correct empty state. QA data removed.
- Tori’s fruit menu tab showed only the strawberry add-on. Source menu, price notes and address displayed.
- Personal tasting note saved, survived reload and was deleted through the UI. QA data removed.
- Area filter Clayton selected Chayō and changed the map iframe URL and directions to 351 Clayton Road.
- A local suggestion was saved, export became enabled and the test suggestion was deleted through the UI.

Limits:

- Visual browser QA used the desktop viewport. Responsive breakpoints at 1050, 800 and 600px are implemented; a separate physical/mobile viewport was not available in this session.
- Google Maps is external and loads asynchronously; direct directions remain available.
- Prices and hours are source snapshots, not in-store verification or live inventory. Four locations intentionally have no confirmed online price.
