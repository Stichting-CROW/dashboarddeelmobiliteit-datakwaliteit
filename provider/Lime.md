# Data quality: Lime

## Data quality status

Last checked 2026-03-17.

| **Quality check**           | **Quality**
| --                          | --                  |
| Uses data standard?         | ✅ MDS
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ✅
| Offers service areas        | ❌

Status: 🟢 Perfect

## Improvements to make

- Offer a MDS feed index that contains all municipalities in The Netherlands, instead of offering 1 data feed per municipality
- Offer a GBFS 3.0 datafeed with the service areas (geofencing_zones.json)

## Logs

| Updated    | Description
| ----       | ---
| 2026-03-09 | 🎉 De Lime-voertuigdata van Zwolle is vanaf vandaag zichtbaar in het Dashboard
| 2026-01-28 | 🎉 De Lime-voertuigdata van Utrecht is vanaf vandaag zichtbaar in het Dashboard
| 2026-01-14 | 🐛 We vragen Lime de authenticatietoken voor het ophalen van Lime-voertuigen in Utrecht. Momenteel ontvangen we nog _geen_ data van Lime Utrecht, terwijl Lime er wel actief is sinds het begin van januari 2026
| 2026-01-14 | 🎉 Het aantal verhuringen van Lime in Tilburg kloptte niet sinds 11 november, door een fout in het Dashboard Deelmobiliteit. Vanaf 13 januari 2026 in de avond worden de verhuringen van Lime weer juist bijgehouden. We kunnen de verhuringen niet met terugwerkende kracht opslaan en zullen de verhuringendata van Lime in Tilburg tussen 11 november 2025 en 14 januari 2026 daarom mogelijk helemaal verwijderen
| 2025-11-11 | 🐛 Sinds 11 november klopt het aanbod van Tilburg wel, maar het aantal verhuringen is vele malen hoger dan wat reeel zou zijn (12 november 2025: 240000 verhuringen op 200 voertuigen. 12 januari 2026: 70000 verhuringen op 200 voertuigen)
| 2025-11-11 | 🎉 Voertuigdata van Tilburg toegevoegd aan het Dashboard Deelmobiliteit
| 2024-07-04 | We hebben de voertuigaantallen van Lime intern vergeleken met die in het Dashboard Deelmobiliteit, voor de periode 30 juni t/m 1 juli 2024. Conclusie is dat er bij Lime intern +4% tot +7% meer voertuigen gerapporteerd worden dan in het Dashboard Deelmobiliteit. De data in de MDS-feed lijkt wel dezelfde aantallen te geven als die in het Dashboard Deelmobiliteit staan. Het zijn relatief kleine verschillen, we proberen nog achter de oorzaak van het verschil te komen.
| 2024-01-23 | We hebben de aantallen van Lime en het Dashboard Deelmobiliteit vergeleken. We keken eerst naar september 2023 in Rotterdam. Het Dashboard rapporteerde 251 Limes, Lime rapporteerde 400 voertuigen. We kijken vervolgens naar 22 januari 2024. Het Dashboard rapporteerde 439, Lime rapporteerde 500. Dit zijn verschillen die we gaan uitzoeken.
