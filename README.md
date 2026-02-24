# Static HTML Homepage

This folder contains a static HTML version of the homepage (no React or build step).

## Viewing the page

1. **Copy assets** from the React app so images and logos load:
   ```bash
   mkdir -p static/assets
   cp src/assets/htg-logo-dark.svg src/assets/megaphone.png src/assets/samsung-neo-qled.png src/assets/synology-ds225.png src/assets/bambu-lab-ams2.png src/assets/horizon-20-projector.png src/assets/ubigi-logo.png src/assets/surfshark-logo.png static/assets/
   ```

2. **Open in a browser** (from project root):
   ```bash
   open static/index.html
   ```
   Or serve the `static` folder with any static server, e.g.:
   ```bash
   npx serve static
   ```

## Files

- **index.html** — Homepage markup (header, hero, subscriber strip, featured offers, category grid, footer).
- **css/home.css** — All styles (variables, layout, components). No Tailwind or build step.
- **assets/** — Images and logos (copy from `src/assets` as above).

## Notes

- Forms (newsletter / “Get deals first”) are plain HTML forms; point `action` to your backend or a form service if you want submissions.
- Hub links (Samsung, Synology, Bambu Lab, XGIMI) point to `samsung.html`, `synology.html`, etc. Add those pages as static HTML when you convert more routes.
- External links (Ubigi, Surfshark, HTG Depot) use full URLs and `target="_blank"`.
