# Data quality: BAQME

## Data quality status

Last check: 2026-05-21.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ MDS 2.0
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ✅
| Shares service areas        | ❌

Status: 🟢 Perfect

## Improvements to make

### Bied 1 MDS-feed aan voor heel Nederland

Momenteel worden 6 MDS-feeds aangeleverd, voor elke vloot 1. Liever ontvangen we 1 MDS-feed met alle NL voertuigen.

## Logs

| Updated    | Description
| ----       | ---
| 2026-05-19 | 🎉 BAQME heeft diens datafeed geupdate, waardoor de verhuringen weer correct worden geregistreerd. De Joyride-feed is nog niet naar de Nederlandse data-standaarden, maar door deze maatoplossing door BAQME hebben we voor BAQME weer data 🙌
| 2026-05-19 | ⏳ Dashboard Deelmobiliteit team heeft een [verzoek](https://github.com/openmobilityfoundation/mobility-data-specification/issues/981) voor de MDS-standaard ingediend, voor betere richtlijnen over het niet gebruiken van paginering. We hopen dat deze suggestie op termijn in de MDS-standaard komt
| 2026-05-04 | BAQME mailt ons pro-actief dat de verhuringenaantallen in het Dashboard Deelmobiliteit niet meer kloppen sinds +- 24 april
| 2026-04-24 | 🐛 Het aantal BAQME-verhuringen klopt niet meer (aantal verhuringen zijn veel te laag). Dit komt door de nieuwe MDS 2.0 feed die Joyride opeens als vervanging online plaatste voor de goed werkende datafeed, zonder iemand daarover te informeren
| 2026-04-24 | 🎉 De datafeed is weer online sinds vandaag 17:55. We gebruiken de nieuwe MDS 2.0 feed
| 2026-04-21 | 🐛 De datafeed van BAQME is offline sinds 21 april 2026 om 09:45 uur. Software-aanbieder Joyride heeft de datafeed-versie geupdate zonder BAQME van tevoren te informeren. In plaats van een MDS 1.2.0 feed is er nu opeens [een MDS 2.0 feed](https://swagger.joyride.tech/mds/) die qua URL-structuur niet de standaard MDS-structuur volgt. Hierdoor kan de feed niet ingeladen worden in het Dashboard Deelmobiliteit zonder dat software-aanpassingen nodig zijn. 
| 2024-01-22 | Otto deed een datakwaliteitscontrole aan de hand van de aantallen in het Dashboard en de aantallen van BAQME. BAQME rapporteerde een totaal aantal voertuigen van 316 op 17 januari 2024. In het Dashboard stonden dezelfde aantallen m.u.v. een kleine afwijking in Ede (afwijking: 2) en Rotterdam (afwijking: 18). De datakwaliteit is goed op orde.
