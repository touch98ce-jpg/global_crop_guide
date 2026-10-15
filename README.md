# Global Crop Guide (prototype, 2026-10-14)

Personal, non-commercial. English. Works as one HTML file with no server — same approach as the Korean beta page.

Files
- index.html — the page. Open by double-click (file://) or put on GitHub Pages.
- fetch_faostat_top_crops.py / .bat — run on the PC once (and again when FAOSTAT updates, yearly). Writes faostat_top_crops.js (top 15 crops per country: production, area, yield, producer price USD/t) and data/faostat_top_crops.json. The page reads the .js file; without it, block 3 and 4 show "not built yet".

Data used by the page (all free, no API key)
- OpenStreetMap Nominatim — place name -> coordinates (1 request/second policy; light use only).
- Open-Meteo Historical Weather API — last 10 complete years of daily tmax/tmin/tmean/precipitation, averaged in the browser. Non-commercial use only.
- FAO FAOSTAT — country-level crops (QCL) and producer prices (PP), CC BY 4.0.

Not in this version (ideas for later): soil (ISRIC SoilGrids 250 m — its point API is paused as of Oct 2026, would need the map files), crop-by-crop climate fit, Google Maps picker (needs a billing account even on the free tier).

Rules carried over from the Korean project: no invented numbers ("no data" instead), every block names its source, user assumptions (costs) are labelled as assumptions.
