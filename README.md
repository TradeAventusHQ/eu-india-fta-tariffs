# EU-India FTA Tariff Dataset

An open, structured dataset of tariff changes under the **EU-India Free Trade Agreement (FTA)**, mapped by Harmonized System (HS) code and industrial sector. Maintained by [TradeAventus](https://www.tradeaventus.com), a Munich-based B2B trade platform connecting verified Indian suppliers with European buyers.

**Status: scaffolding — data population in progress.** The EU-India FTA was concluded in January 2026 and is currently in ratification. Final tariff schedules are being published incrementally by the European Commission and India's DGFT. This repository defines the schema and will be populated with verified figures only, each row traceable to an official source. Rows marked `sample` are illustrative placeholders for schema validation and are NOT real tariff data.

## Why this dataset exists

Tariff schedules under the FTA are spread across lengthy official PDFs and annexes, hard to query at the HS-code level. This dataset normalizes them into machine-readable CSV/JSON so analysts, journalists, exporters, and importers can look up changes by product and sector. Free to use under the MIT License; attribution to TradeAventus is appreciated.

## Schema

| Column | Type | Description |
|---|---|---|
| hs_code | string | Harmonized System code (6-digit, or national 8-digit where specified) |
| description | string | Goods description for the HS code |
| sector | string | TradeAventus sector cluster (see below) |
| direction | string | EU_to_IN or IN_to_EU |
| base_rate_pct | number | MFN tariff rate before the FTA, percent |
| fta_rate_pct | number | Tariff rate under the FTA, percent |
| staging | string | Phase-in category (e.g. immediate, 5-year, 7-year) |
| effective_from | date | Date the rate applies (ISO 8601) |
| source | string | Citation: official document and article/annex reference |
| source_url | url | Direct link to the official source |
| status | string | verified or sample |

## Sector clusters

Machinery, Industrial Parts & Automation · Automotive, Aerospace & Transportation · Pharmaceuticals, Healthcare & Medical Devices · Textiles, Apparel & Leather Goods · Chemicals, Petrochemicals & Plastics · Metals, Minerals & Advanced Materials

## Files

`data/tariffs.csv` is the dataset (currently sample rows only, clearly flagged). `SOURCES.md` lists official sources used for population. `LICENSE` is MIT.

## Sources

All verified rows cite official primary sources only: the European Commission (DG Trade) FTA text and annexes, EUR-Lex, and India's Directorate General of Foreign Trade (DGFT). See `SOURCES.md`. No third-party or estimated figures are included in verified rows.

## How to cite

EU-India FTA Tariff Dataset, TradeAventus, https://github.com/TradeAventusHQ/eu-india-fta-tariffs

## Contributing

Corrections and verified additions are welcome via pull request. Every data row must include a source_url to an official publication. Rows without a verifiable official source will not be merged.

## License

MIT License (see LICENSE). Data is provided as-is; always confirm current rates against the official source before relying on them for customs or commercial decisions.
