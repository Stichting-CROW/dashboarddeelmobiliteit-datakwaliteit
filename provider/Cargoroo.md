# Data quality: Cargoroo

## Data quality status

Last checked: 2026-04-23.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ MDS
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ❌
| Includes vehicle type?      | ❌
| Offers service areas        | ❌

Status: 🔴 Unusable

## Improvements to make

### Volg de MDS-standaard voor URL's

Momenteel wordt niet de standaard MDS URL-structuur gebruikt, maar dient er met query parameters aangegeven te worden welke feed geladen wordt. In plaats daarvan: volg de standaard URL-structuur

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
| 2026-04-21 | 🐛 De datafeed van Cargoroo is offline sinds 21 april 2026 om 09:45 uur. Software-aanbieder Joyride heeft de datafeed-versie plotseling geupdate. In plaats van een MDS 1.2.0 feed is er nu opeens [een MDS 2.0 feed](https://swagger.joyride.tech/mds/) die qua URL-structuur niet de standaard MDS-structuur volgt. Hierdoor kan de feed niet ingeladen worden in het Dashboard Deelmobiliteit zonder dat software-aanpassingen nodig zijn. 
| 2026-01-26 | Cargoroo (by MOBY) voertuigen vanaf nu zichtbaar voor Den Haag. We ontvangen nog geen Utrecht data en nog geen servicegebieden
| 2025-01-15 | We hebben de datafeed uitgezet, omdat Cargoroo niet meer actief is in Nederland |
