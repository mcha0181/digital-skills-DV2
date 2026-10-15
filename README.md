# Australia’s digital skills divide — revised FIT3179 site

Upload `index.html`, the entire `charts/` folder and the entire `data/` folder to the ROOT of your public GitHub Pages repository. This package keeps all 11 chart specifications.

## Map reading guide
- Chart 08: interactive tile cartogram. Switch between Digital ability, Access and Affordability using the dropdown. Scores are 0–100.
- Chart 09: circle-area proportional-symbol map of ABS 2021 online Census response %. Plain circles, no emoji; the Vega size legend and caption explain symbol sizes.
- Chart 10: choropleth map of ADII 2025 Digital Ability score, grouped into three explained bands.

**Important:** Map 09 shows the ONLINE CENSUS RESPONSE RATE, not digital ability. It cannot be interpreted as a direct measure of skill. Map 10 contains actual geographic state boundaries loaded from an external GeoJSON source; test the link when publishing.

## Publish
1. Extract ZIP.
2. On GitHub replace root `index.html`, replace `charts/chart01.json` through `chart11.json` and upload the included `data` files.
3. Commit changes.
4. Wait for Pages deployment then hard refresh.
5. Confirm 11 charts and all three maps render; test tile dropdown and mouseover legends.
6. Replace `YOUR NAME` in index.html and acknowledge assistance.

## Data
Source values remain those in the previous supplied project. Original datasets: Australian Digital Inclusion Index (2025), ABS Census collection methodology (2021). Group scores reconstructed from published contrasts and explicitly indicated. For source citations see `index.html`.
