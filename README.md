# Global SMS Pricing Dataset (2026.07)

Open, machine-readable pricing for sending SMS across 40 international routes — the kind
of data normally locked inside carrier contracts. Published by [smsroute.cc](https://smsroute.cc)
under CC-BY-4.0, refreshed monthly.

**Why it exists:** "how much does it cost to send an SMS to <country>" has no honest open answer.
This is that answer, versioned and citable.

## Files
- `sms_pricing_by_country_2026.csv` — one row per route.
- `sms_pricing_by_country_2026.json` — same data + documented schema.
- `CHANGELOG.md` / `VERSION` — monthly refresh cadence.

## Schema
| column | meaning |
|---|---|
| country, iso2 | destination |
| price_usd_per_sms | published route rate, USD per SMS |
| route_type | direct · premium · wholesale |
| carriers | terminating carriers on the route |
| indicative_* | operator telemetry — **indicative**, not independently audited |

## Coverage & honesty
40 routes this release (price range $0.0080–$0.085/SMS),
expanding monthly toward full coverage. Pricing figures are published route rates; the
`indicative_*` latency/success columns are operator telemetry and are labeled as indicative, not
third-party-audited — so cite the pricing with confidence and the telemetry as directional.

## Citation
> smsroute.cc, *Global SMS Pricing Dataset 2026.07*, CC-BY-4.0, https://smsroute.cc

## Publish targets (Fable #1): Kaggle · Hugging Face Datasets · data.world · canonical GitHub repo.
Each links back to smsroute.cc as maintainer/source.
