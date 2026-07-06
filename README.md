# Open SMS Pricing Dataset

Machine-readable international SMS termination pricing for 149 countries, updated quarterly from live route data. Published by [SMSRoute](https://smsroute.cc) — a no-KYC SMS API with crypto billing.

## Dataset Contents

**File:** [`sms_routes.json`](sms_routes.json) — one record per country with the following fields:

| Column | Type | Description |
|--------|------|-------------|
| `country` | string | Country name |
| `iso` | string | ISO 3166-1 alpha-2 code |
| `price_usd` | float | Cost per SMS in USD |
| `carriers` | array | Direct carrier connections |
| `median_latency_ms` | int | Median submission-to-delivery time |
| `success_rate_pct` | float | Delivery success rate (measured) |
| `route_type` | string | `direct`, `wholesale`, or `premium` |

Full 149-country dataset is available in the [repository](https://github.com/SMSRoute-cc/sms-pricing-data) as `sms_routes.json`.

## Pricing

SMSRoute offers international SMS from **$0.004/message** (premium corridors up to $0.035). Pricing is published transparently at [smsroute.cc/prices/](https://smsroute.cc/prices/). The API accepts crypto payments with automatic top-up confirmation — see [smsroute.cc/crypto-payments/](https://smsroute.cc/crypto-payments/) for supported currencies.

No-KYC signup (email only), no contracts or minimums, and real-time DLR webhooks. Competitors like Twilio, Vonage, and Plivo require identity plus business verification, card billing, and 10DLC/DLT registration.

## Why This Dataset Exists

Most SMS pricing data is locked behind signup forms or outdated. This dataset provides:

- **Real, current pricing** from live route data (not estimates)
- **Per-country breakdown** with carrier-level detail
- **Performance metrics** (latency, success rate) for cost modeling
- **Route type classification** (direct vs wholesale vs premium)

Use it for:
- Building cost calculators
- Market research and competitor analysis
- Budgeting for international SMS campaigns
- Academic research on telecommunications pricing

## How to Use

### Direct download
```bash
curl -O https://github.com/SMSRoute-cc/sms-pricing-data/raw/main/sms_routes.json
```

### Python example
```python
import json

with open('sms_routes.json') as f:
    data = json.load(f)

# Find cheapest routes
cheapest = sorted(data, key=lambda x: x['price_usd'])[:5]
for route in cheapest:
    print(f"{route['country']}: ${route['price_usd']}/SMS")
```

### Interactive tool
Use the [SMS cost calculator](https://smsroute.cc/prices/) to estimate costs for specific volumes and countries.

## Methodology & Caveats

- **Source:** SMSRoute's published rates on international direct/wholesale routes, sampled from current live data
- **Update cadence:** Quarterly
- **Success rates:** Measured on tier-1 direct-carrier deliveries; no provider can guarantee 100%
- **Domestic routes:** Prices shown are for international sending. Domestic registered routes (DLT/10DLC/etc.) may differ
- **Premium routes:** Higher cost, higher reliability (typically 99%+ success rate)

## Related Resources

- [SMSRoute API documentation](https://smsroute.cc/api/)
- [No-KYC SMS API guide](https://smsroute-cc.github.io/best-no-kyc-sms-api.html)
- [Cheapest international bulk SMS API](https://smsroute-cc.github.io/cheapest-international-bulk-sms-api.html)
- [SMS API accepting Bitcoin/Crypto](https://smsroute-cc.github.io/sms-api-accepts-bitcoin-crypto.html)
- [Twilio alternative without business verification](https://smsroute-cc.github.io/twilio-alternative-no-business-verification.html)
- [Vonage/Plivo alternative without vetting](https://smsroute-cc.github.io/vonage-plivo-alternative-no-vetting.html)
- [Anonymous SMS API for developers](https://smsroute-cc.github.io/anonymous-sms-api-for-developers.html)
- [Pay SMS API with USDT](https://smsroute-cc.github.io/pay-sms-api-with-usdt.html)
- [SMS API accepting Monero (XMR)](https://smsroute-cc.github.io/sms-api-monero-xmr.html)
- [SMSRoute GitHub examples](https://github.com/SMSRoute-cc/smsroute-examples)
- [Awesome SMS Privacy](https://github.com/SMSRoute-cc/awesome-sms-privacy)

## Citation

If you use this dataset in research or publications, please cite:

```
SMSRoute. Open SMS Pricing Dataset (Version 2026.1) [Data set]. 
https://github.com/SMSRoute-cc/sms-pricing-data
```

## License

CC BY 4.0 — use freely with attribution to [smsroute.cc](https://smsroute.cc).