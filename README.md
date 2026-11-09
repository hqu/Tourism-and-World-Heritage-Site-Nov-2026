# Tourism and World Heritage

An interactive dashboard comparing international tourist arrivals across countries and regions, and exploring how UNESCO World Heritage sites relate to tourism.

**Live site:** https://hqu.github.io/Tourism-and-World-Heritage-Site-Nov-2026/

## What it shows

- **Fastest growth.** Average yearly growth in arrivals for 2009–2019 or 1995–2019, by World Bank region and by country. The fastest-growing region and country are highlighted. A country needs at least 1 million arrivals at the start of the period to be ranked.
- **Regional trends.** Arrivals by region, indexed to the start year.
- **Heritage and tourism.**
  - A scatter plot of World Heritage sites against 2019 arrivals, and of sites added from 2010 to 2019 against growth over the same decade.
  - Median arrivals by number of sites.
  - Countries with the most and fewest visitors per site.
  - A map of all sites.
- **Compare places.** Arrivals per year, 1995–2020, for any countries or regions you pick.

## Data

| File | Source |
| --- | --- |
| `data/tourism_arrivals.csv` | World Bank, World Development Indicators: *International tourism, number of arrivals* (ST.INT.ARVL), last updated 8 October 2026 |
| `data/heritage_sites.json` | UNESCO World Heritage List export (whc001): 1,273 sites with inscription year, category, danger status, countries and coordinates. ISO country codes were matched to World Bank codes. |

### Notes on the data

- Growth rates use only years up to 2019. In 2020 the pandemic cut arrivals sharply, and only 132 places reported that year.
- Comparisons with 2019 arrivals count only sites inscribed by 2019.
- A site shared by several countries counts once for each country.
- These figures show correlation, not causation. Large, well-connected countries tend to have both many sites and many visitors.

## Running locally

The page loads its data with `fetch`, so serve the folder instead of opening the file directly:

```bash
python -m http.server
```

Then open http://localhost:8000.
