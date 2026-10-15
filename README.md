# Australia's digital skills divide · FIT3179

Single public GitHub Pages web page, with 10 Vega-Lite specs and CSV source tables.

## Publish (click by click)
1. Sign in at https://github.com and click **+ → New repository**.
2. Name the repository `digital-skills-australia`, set **Public**, then click **Create repository**.
3. Choose **Add file → Upload files**. Drag and drop **the contents** of this extracted folder (including the `charts` and `data` folders), not the ZIP file. Press **Commit changes**.
4. Open **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
5. Choose **Branch: main**, **Folder: /(root)**, click **Save**.
6. Wait a minute and visit `https://YOUR-USERNAME.github.io/digital-skills-australia/`.
7. Open the page on mobile/small laptop, confirm 10 charts appear.
8. Change `YOUR NAME` in `index.html` to your own name and commit.

## Edit each Vega-Lite chart (click by click)
1. Go to https://vega.github.io/editor/ and choose **Vega-Lite** (top left).
2. Open `charts/chart01.json` inside the GitHub repo, click **Raw**, copy all text.
3. Paste into the left editor panel, replacing its starter text.
4. The charts reference relative `data/*.csv` URLs; **for Editor preview**, change the `data.url` field to the absolute GitHub Pages URL, e.g. `https://YOUR-USERNAME.github.io/digital-skills-australia/data/states_2025.csv`.
5. Wait for preview. Edit chart title, field or encoding. Copy finished JSON back into its corresponding `charts/chart01.json` file using GitHub pencil icon → Commit changes.
6. Repeat for chart02 to chart10, using source-data filename shown in each JSON. Chart09 and 10 have TWO `data.url` fields; only change the `data/*.csv` one, not the `world-110m.json` URL.

## Chart and data correspondence
|Chart|Spec|Data CSV|Chart kind|
|--|--|--|--|
|1|chart01.json|states_2025.csv|Horizontal bar: state ability|
|2|chart02.json|skills_time.csv|Line: 2023 to 2025|
|3|chart03.json|group_comparison.csv|Bar: age groups|
|4|chart04.json|group_comparison.csv|Bar: educational groups|
|5|chart05.json|ability_gaps.csv|Bar: group gaps|
|6|chart06.json|states_2025.csv|Heat map: three dimensions|
|7|chart07.json|census_online.csv|Line: Census online completion|
|8|chart08.json|states_2025.csv|Tile-grid cartogram|
|9|chart09.json|states_2025.csv|Graduated-symbol geographic map|
|10|chart10.json|states_census_map.csv|Geographic square-symbol map|

## Sources and important warnings
- [Australian Digital Inclusion Index (2025)](https://digitalinclusionindex.org.au/wp-content/uploads/2025/10/ADII-Report-2025_V6-Remediated.pdf), p. 12 state values and p. 8/16 national and subgroup values. ADII data is CC BY-NC-SA 4.0; cite Thomas et al. (2025).
- [ABS (2021) Census collection methodology](https://www.abs.gov.au/census/guide-census-data/census-methodology/2021/how-data-collected), mode of response table for 2011/2016/2021.
- `group_comparison.csv`: 18–34 = 41.5+47.4 = 88.9; university = 54.4+28.3 = 82.7 (both *derived* from published gaps; no invented values).
- The ABS indicator is online form completion, not digital skill. Maps 9 and 10 mark approximate locations for states/territories.
- 2025 affordability score definition changed: **do not compare it to earlier years**.
- Check the three map idioms against your tutor's interpretation; a tile-grid cartogram plus two symbol map variants may not satisfy a requirement for three *different* idioms at a high grade. For strict compliance, replace one symbol map with a genuine state choropleth using validated state boundaries.
- The assignment also needs a separately uploaded scanned **hand-drawn A4 sketch PDF** URL and a domain/who/what/why/how description.

## Three different map idioms
- Chart 08: tile-grid cartogram (equal-sized state tiles).
- Chart 09: proportional-symbol map (circle size = Digital Ability).
- Chart 10: choropleth map (state shape fill = ABS online Census response percentage).

Chart 10 uses Australian state boundaries from https://github.com/rowanhogan/australian-states (external GeoJSON). The GeoJSON is loaded remotely, so the viewer needs internet access.

To edit in Vega Editor, replace any `data/...csv` URL in the JSON with `https://YOUR-USERNAME.github.io/digital-skills-australia/data/...csv`; after testing, restore the relative path when committing the specification to GitHub Pages.
