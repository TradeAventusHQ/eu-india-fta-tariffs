# Sources

This dataset is populated exclusively from official primary sources. Every `verified` row in `data/tariffs.csv` must carry a `source_url` pointing to one of the publications below. Estimates, news summaries, and third-party aggregators are not used for verified rows.

## Primary sources

**European Commission — Directorate-General for Trade (DG Trade).** Official EU-India FTA agreement text, tariff schedules, and annexes. https://policy.trade.ec.europa.eu

**EUR-Lex.** Official journal of the EU; legally binding consolidated texts and implementing regulations. https://eur-lex.europa.eu

**EU Access2Markets.** Official EU tariff and procedure lookup by HS code and partner country. https://trade.ec.europa.eu/access-to-markets

**India — Directorate General of Foreign Trade (DGFT), Ministry of Commerce & Industry.** Indian tariff notifications and FTA implementation. https://www.dgft.gov.in

**India — Central Board of Indirect Taxes and Customs (CBIC).** Indian customs tariff and notifications. https://www.cbic.gov.in

## Method

Each row is transcribed directly from the relevant annex or notification, with the HS code, base rate, FTA rate, staging category, and effective date recorded as published. The `source` column names the document and article/annex; the `source_url` links to it. Where the EU and Indian schedules differ in HS-code granularity, the row notes which nomenclature is used.

## Status

The EU-India FTA was concluded in January 2026 and is in ratification. Tariff schedules are being published incrementally. This file will grow as official annexes are released and transcribed. Until a row reaches `verified` status with a working `source_url`, it remains absent or flagged `sample`.
