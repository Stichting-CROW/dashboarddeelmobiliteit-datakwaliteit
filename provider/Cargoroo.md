# Data quality: Cargoroo

## Data quality status

Last checked at 2026-01-26.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ MDS
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ❌
| Includes vehicle type?      | ❌
| Offers service areas        | ❌

Status: 🟡 Usable though needs improvement

### Explanation

- The data feed uses MDS 👍
- The feed is updated frequently 👍
- Cargoroo offers data of all vehicles 👍
- Cargoroo does not offer 'vehicle type' in their data feed yet (not super important as all are cargo bikes) ❌
- Cargoroo does not offer all vehicles in The Netherlands but only those of The Hague ❌
- Cargoroo does not offer service areas yet using GBFS ([technical documentation](https://docs.dashboarddeelmobiliteit.nl/data_feeds/service_areas/))

## Logs

| Updated    | Description
| ----       | ---
| 2026-01-26 | Cargoroo (by MOBY) voertuigen vanaf nu zichtbaar voor Den Haag. We ontvangen nog geen Utrecht data en nog geen servicegebieden
| 2025-01-15 | We hebben de datafeed uitgezet, omdat Cargoroo niet meer actief is in Nederland |
