# EU CBAM default values

The EU's official CBAM default values as machine-readable JSON and CSV: direct, indirect and total embedded emissions (t CO2e per tonne of good) for every CN code and every country listed in Annex I, plus "Other countries and territories" and Annex IV (precursors of unknown origin). 11,170 rows, 121 countries. Also the Column A and B benchmarks with the CBAM factor for each year.

Files:

- [`default-values.json`](default-values.json): every table, keyed by country, with each CN code's description, sector, direct, indirect and total value and production route, plus the mark-ups per year.
- [`default-values.csv`](default-values.csv): the same default values as one CSV (`table, cn, description, sector, direct, indirect, total, route`).
- [`benchmarks.json`](benchmarks.json): Column A and B benchmarks per CN code and production route, with the CBAM factor for each year.

Look up a value with the mark-up already applied, per country or per CN code: **[CBAM default values on the CBAM Exporter Pack](https://cbam.vedacta.com/cbam-default-values)** (for example [India](https://cbam.vedacta.com/cbam-default-values/india), [China](https://cbam.vedacta.com/cbam-default-values/china), [Türkiye](https://cbam.vedacta.com/cbam-default-values/turkiye)). The same files are served for ERP systems at [cbam.vedacta.com/cbam-data-feed](https://cbam.vedacta.com/cbam-data-feed), which is updated first.

## Using the values

Value for a good = total default value (direct where there is no total) × (1 + mark-up): 10% in 2026, 20% in 2027, 30% from 2028, 1% for fertilisers. A country that is not listed, or a good without a value for its country, uses "Other countries and territories". Annex IV applies only to precursors whose country of production is unknown.

Free allocation deducted per tonne = CBAM factor × Column B benchmark of the default value's route. To see what this costs per shipment, use the free [CBAM cost calculator](https://cbam.vedacta.com/cbam-cost-calculator).

## Source

- Default values: Implementing Regulation (EU) 2025/2621, Annex I and IV, as corrected by Implementing Regulation (EU) 2026/1740; Commission file "DV correcting act_final update_06.08.xlsx" (6 August 2026).
- Benchmarks: Implementing Regulation (EU) 2025/2620; Commission file "CBAM Benchmarks_20260206.xlsx".

Both from the Commission's [CBAM legislation and guidance](https://taxation-customs.ec.europa.eu/carbon-border-adjustment-mechanism/cbam-legislation-and-guidance_en) page. Every value is checked against those files value by value before release. Files copied from the data feed on 29 October 2026.

Unofficial compilation, not affiliated with or endorsed by the EU, provided as is. The Official Journal texts are binding: check values there before you rely on them.

## Licence

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), commercial use included. Credit "CBAM Exporter Pack (cbam.vedacta.com), based on European Commission data © European Union". The EU data is reused under Commission Decision 2011/833/EU.

Maintained by [Vedacta](https://vedacta.com/). Found an error? Open an issue.
