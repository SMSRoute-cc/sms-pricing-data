# Open SMS Pricing Dataset (2026)

Machine-readable SMS termination pricing, carrier routes, and delivery metrics for 40 countries. Published by [smsroute.cc](https://smsroute.cc) from live route data.

**Files**: [`sms_routes.json`](sms_routes.json) — one record per country: price (USD), direct carrier list, median submission latency (ms), delivered success rate (%), route type.

Use it for cost models, market research, or benchmarks. Interactive version: [SMS cost calculator](https://smsroute.cc/tools/sms-cost-calculator).

| Country | ISO | $/SMS | Carriers | Median ms | Success % | Route |
|---|---|---|---|---|---|---|
| Argentina | AR | 0.029 | Claro, Movistar, Personal | 106 | 97.7 | direct |
| Australia | AU | 0.028 | Telstra, Optus, Vodafone | 93 | 98.8 | direct |
| Bangladesh | BD | 0.013 | Grameenphone, Robi, Banglalink | 128 | 96.4 | wholesale |
| Brazil | BR | 0.018 | Vivo, Claro, TIM | 104 | 98.1 | direct |
| Canada | CA | 0.015 | Rogers, Bell, Telus | 89 | 98.9 | direct |
| Chile | CL | 0.025 | Movistar, Claro, Entel | 97 | 98.2 | direct |
| Colombia | CO | 0.022 | Claro, Movistar, Tigo | 101 | 97.9 | direct |
| Egypt | EG | 0.018 | Orange, Vodafone, Etisalat | 110 | 97.8 | direct |
| France | FR | 0.075 | Orange, SFR, Bouygues Telecom | 86 | 99.0 | premium |
| Germany | DE | 0.085 | Deutsche Telekom, Vodafone, O2 | 84 | 99.2 | premium |
| Ghana | GH | 0.019 | MTN, Vodafone, AirtelTigo | 120 | 96.7 | direct |
| India | IN | 0.012 | Jio, Airtel, Vi | 102 | 98.0 | direct |
| Indonesia | ID | 0.023 | Telkomsel, Indosat, XL Axiata | 107 | 97.6 | direct |
| Israel | IL | 0.035 | Cellcom, Partner, Pelephone | 92 | 98.5 | direct |
| Italy | IT | 0.048 | TIM, Vodafone, Wind Tre | 90 | 98.6 | direct |
| Japan | JP | 0.065 | NTT Docomo, KDDI, SoftBank | 94 | 98.9 | direct |
| Kenya | KE | 0.014 | Safaricom, Airtel, Telkom | 118 | 96.9 | direct |
| Malaysia | MY | 0.027 | Maxis, Celcom, Digi | 96 | 98.3 | direct |
| Mexico | MX | 0.02 | Telcel, Movistar, AT&T | 100 | 98.0 | direct |
| Morocco | MA | 0.035 | Maroc Telecom, Orange Maroc | 95 | 98.6 | direct |
| Netherlands | NL | 0.055 | KPN, Vodafone, T-Mobile | 83 | 99.1 | direct |
| Nigeria | NG | 0.016 | MTN, Airtel, Glo | 115 | 97.0 | direct |
| Pakistan | PK | 0.011 | Jazz, Zong, Telenor | 125 | 96.5 | wholesale |
| Peru | PE | 0.024 | Claro, Movistar, Entel | 99 | 98.0 | direct |
| Philippines | PH | 0.026 | Globe, Smart, DITO | 109 | 97.4 | direct |
| Poland | PL | 0.032 | Orange, Play, T-Mobile | 92 | 98.4 | direct |
| Russia | RU | 0.022 | MTS, Beeline, MegaFon | 112 | 96.8 | wholesale |
| Saudi Arabia | SA | 0.05 | STC, Mobily, Zain | 85 | 98.9 | premium |
| Singapore | SG | 0.03 | Singtel, StarHub, M1 | 86 | 99.0 | direct |
| South Africa | ZA | 0.024 | Vodacom, MTN, Cell C | 98 | 98.2 | direct |
| South Korea | KR | 0.06 | SK Telecom, KT, LG U+ | 88 | 99.1 | direct |
| Spain | ES | 0.042 | Movistar, Vodafone, Orange | 88 | 98.7 | direct |
| Sri Lanka | LK | 0.017 | Dialog, Mobitel, Airtel | 122 | 96.8 | direct |
| Thailand | TH | 0.021 | AIS, TrueMove, dtac | 103 | 97.9 | direct |
| Turkey | TR | 0.02 | Turkcell, Vodafone, Türk Telekom | 105 | 97.5 | direct |
| Ukraine | UA | 0.025 | Kyivstar, Vodafone, lifecell | 108 | 97.2 | wholesale |
| United Arab Emirates | AE | 0.045 | Etisalat, du | 82 | 99.0 | premium |
| United Kingdom | GB | 0.038 | EE, Vodafone, O2 | 91 | 99.0 | premium |
| United States | US | 0.008 | AT&T, Verizon, T-Mobile | 87 | 99.1 | premium |
| Vietnam | VN | 0.015 | Viettel, Mobifone, Vinaphone | 126 | 96.6 | wholesale |

## Method & caveats
Prices are smsroute.cc published rates on international direct/wholesale routes, sampled 2026. Domestic registered routes (DLT/10DLC/etc.) price differently. Success rates are measured on tier-1 direct-carrier deliveries; no provider can promise 100%.

## License
CC BY 4.0 — use freely with attribution to smsroute.cc.
