# Data quality: BAQME

## Data quality status

Last check: 2026-04-21.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ❌ MDS 2.0
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ✅
| Shares service areas        | ❌

Status: 🔴 Unusable

## Improvements to make

### Volg de MDS-standaard voor URL's

Momenteel wordt niet de standaard MDS URL-structuur gebruikt, maar dient er met query parameters aangegeven te worden welke feed geladen wordt. In plaats daarvan: volg de standaard URL-structuur

### Bied 1 MDS-feed aan voor heel Nederland

Momenteel worden 6 MDS-feeds aangeleverd, voor elke vloot 1. Liever ontvangen we 1 MDS-feed met alle NL voertuigen.

## Logs

| Updated    | Description
| ----       | ---
| 2026-04-21 | 🐛 De datafeed van BAQME is offline sinds 21 april 2026 om 09:45 uur. Software-aanbieder Joyride heeft de datafeed-versie geupdate zonder BAQME van tevoren te informeren. In plaats van een MDS 1.2.0 feed is er nu opeens [een MDS 2.0 feed](https://swagger.joyride.tech/mds/) die qua URL-structuur niet de standaard MDS-structuur volgt. Hierdoor kan de feed niet ingeladen worden in het Dashboard Deelmobiliteit zonder dat software-aanpassingen nodig zijn. 
| 2024-01-22 | Otto deed een datakwaliteitscontrole aan de hand van de aantallen in het Dashboard en de aantallen van BAQME. BAQME rapporteerde een totaal aantal voertuigen van 316 op 17 januari 2024. In het Dashboard stonden dezelfde aantallen m.u.v. een kleine afwijking in Ede (afwijking: 2) en Rotterdam (afwijking: 18). De datakwaliteit is goed op orde.
