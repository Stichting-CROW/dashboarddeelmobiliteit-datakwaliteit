# Data quality: HTM

## Data quality status

Last updated: 2025-02-12.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ❌ MDS
| Updated <= 30s?             | ➖
| Correct PROW?               | ➖
| All NL data?                | ➖
| Includes vehicle type?      | ➖

Status: 🔴 Unusable

## Logs

| Updated    | Description
| ----       | ---
| 2026-04-21 | 🐛 De datafeed van HTM is offline sinds 21 april 2026 om 09:45 uur. Software-aanbieder Joyride heeft de datafeed-versie plotseling geupdate. In plaats van een MDS 1.2.0 feed is er nu opeens [een MDS 2.0 feed](https://swagger.joyride.tech/mds/) die qua URL-structuur niet de standaard MDS-structuur volgt. Hierdoor kan de feed niet ingeladen worden in het Dashboard Deelmobiliteit zonder dat software-aanpassingen nodig zijn. 
