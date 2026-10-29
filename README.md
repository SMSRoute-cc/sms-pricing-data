# Global SMS pricing dataset (2026-10)

Open, machine-readable prices for sending one SMS across international routes — the data normally
buried in carrier contracts. Published under CC-BY-4.0, refreshed monthly.

**Why it exists:** "how much does it cost to send an SMS to <country>" has no honest open answer. This
is that answer, versioned and citable.

Last verified: 2026-10-29.

## Files

| File | Contents |
|---|---|
| `sms_pricing_by_country_2026.csv` | one row per route |
| `sms_pricing_by_country_2026.json` | same data with a documented schema |
| `CHANGELOG.md` | monthly refresh notes |
| `VERSION` | dataset version |

## Schema

| Column | Meaning |
|---|---|
| `country` | destination country name |
| `iso2` | ISO 3166-1 alpha-2 |
| `price_usd` | price for one one-part (GSM-7, 160 char) message, USD |
| `currency_local` | local currency code |
| `operator_count` | number of connected operators on that route |
| `verified_on` | date this row was checked |

## Coverage

The current release covers the routes below. Missing routes are missing because no verified price was
available — they are not zero.

## How to cite

> SMSRoute, *Global SMS Pricing Dataset*, version 2026-10, https://github.com/SMSRoute-cc/sms-pricing-data

## Caveats

- Prices are one-part GSM-7. Unicode/UCS-2 messages bill per 70 characters, so a message with emoji can
  cost 2–3× the listed price.
- Taxes, sender-ID fees and volume discounts are excluded.
- Prices change; every row carries the date it was verified.

## Licence

CC-BY-4.0 — reuse with attribution.
