# Bathing Water Quality in Europe (1990–2024)

A data visualization project analyzing bathing water quality across 31 European countries
over 35 years, using public data from the European Environment Agency, the World Bank, and
Eurostat. Built as a university project for the Data Visualization course at FMFI UK.

Full write-up: [`report/Bathing_Water_Quality_Report_EN.pdf`](report/Bathing_Water_Quality_Report_EN.pdf)

## The questions

- How has bathing water quality in Europe changed over the past 35 years?
- Are there significant differences between countries and between water types (coastal, inland, transitional)?
- Is water quality related to a country's economic level (GDP)?
- Does coastal tourism intensity affect coastal water quality?

## Data sources

| Source | What | Coverage |
|---|---|---|
| [EEA](https://www.eea.europa.eu/en/topics/in-depth/bathing-water) | Bathing water quality assessments | 672,629 records, 31 countries, 1990–2024 |
| [World Bank](https://data.worldbank.org/indicator/NY.GDP.PCAP.CD) | GDP per capita (USD and PPP) | All countries, 1990–2024 |
| [Eurostat](https://ec.europa.eu/eurostat/databrowser/view/tour_occ_nin2c) | Nights spent at coastal tourist accommodation | 27 countries, 2012–2024 |

## Key findings

- Bathing water quality in Europe has clearly improved: the average quality score fell from
  around 1.8 in 1990 to 1.2 in 2024, and has held steady since 2011.
- A country's GDP is not a strong predictor of its bathing water quality; the correlation is
  weak, likely because EU-wide legislation sets a common bar regardless of a country's wealth.
- Coastal tourism intensity shows no visible link to a decline in coastal water quality, even
  at record tourism levels in 2022–2024.

## Charts

- Country ranking by % of beaches in the Excellent category (2024)
- Choropleth map of bathing water quality across Europe
- Long-term quality trend and a country x year heatmap (1990–2024)
- Country deep-dives for Spain, Italy, Croatia, and Slovakia
- Quality by water type over time
- GDP vs. water quality
- Coastal tourism vs. coastal water quality

## Tech stack

Python, pandas, matplotlib, seaborn, plotly, geopandas, pycountry

## Repository structure

```
project_en.ipynb   Notebook: data loading, cleaning, merging, and all charts (English)
report/            Full written report (PDF)
*.csv / *.xlsx     Raw data downloaded from EEA, World Bank, and Eurostat
```

## Running it locally

```bash
git clone https://github.com/S4mYo/data-visualisation-project.git
cd data-visualisation-project
pip install -r requirements.txt
jupyter notebook project_en.ipynb
```

The notebook downloads the EEA, World Bank, and Eurostat datasets directly from this
repository, and country boundary polygons from a public GeoJSON source, so it can be re-run
end to end with an internet connection.

## Author

Samuel Pollák
