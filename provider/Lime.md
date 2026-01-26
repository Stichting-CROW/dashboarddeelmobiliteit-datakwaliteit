# Data quality: Lime

## Data quality status

Last checked 2026-01-26.

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
| 2026-01-14 | 🐛 We vragen Lime de authenticatietoken voor het ophalen van Lime-voertuigen in Utrecht. Momenteel ontvangen we nog _geen_ data van Lime Utrecht, terwijl Lime er wel actief is sinds het begin van januari 2026
| 2026-01-14 | 🎉 Het aantal verhuringen van Lime in Tilburg kloptte niet sinds 11 november, door een fout in het Dashboard Deelmobiliteit. Vanaf 13 januari 2026 in de avond worden de verhuringen van Lime weer juist bijgehouden. We kunnen de verhuringen niet met terugwerkende kracht opslaan en zullen de verhuringendata van Lime in Tilburg tussen 11 november 2025 en 14 januari 2026 daarom mogelijk helemaal verwijderen
| 2025-11-11 | 🐛 Sinds 11 november klopt het aanbod van Tilburg wel, maar het aantal verhuringen is vele malen hoger dan wat reeel zou zijn (12 november 2025: 240000 verhuringen op 200 voertuigen. 12 januari 2026: 70000 verhuringen op 200 voertuigen)
| 2025-11-11 | 🎉 Voertuigdata van Tilburg toegevoegd aan het Dashboard Deelmobiliteit
| 2024-07-04 | We hebben de voertuigaantallen van Lime intern vergeleken met die in het Dashboard Deelmobiliteit, voor de periode 30 juni t/m 1 juli 2024. Conclusie is dat er bij Lime intern +4% tot +7% meer voertuigen gerapporteerd worden dan in het Dashboard Deelmobiliteit. De data in de MDS-feed lijkt wel dezelfde aantallen te geven als die in het Dashboard Deelmobiliteit staan. Het zijn relatief kleine verschillen, we proberen nog achter de oorzaak van het verschil te komen.
| 2024-01-23 | We hebben de aantallen van Lime en het Dashboard Deelmobiliteit vergeleken. We keken eerst naar september 2023 in Rotterdam. Het Dashboard rapporteerde 251 Limes, Lime rapporteerde 400 voertuigen. We kijken vervolgens naar 22 januari 2024. Het Dashboard rapporteerde 439, Lime rapporteerde 500. Dit zijn verschillen die we gaan uitzoeken.
| 2022-09-09 | Lime shared the MDS feed and credentials with us. From today we re-activated Lime in the Dashboard.
| 2022-09-05 | We email Lime: Can me do a quick call to make the CROW Dashboard Deelmobiliteit integration happen? 
| 2022-08-17 | We answer: "The Lime GBFS feed is disabled as it's using rotating IDs and this is not following the [data feed requirements](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/). We ask to offer a MDS `/vehicles` feed or a GBFS 1.0 `/free_bike_status.json` feed. Please offer one of these, or let us know if you have any questions."
| 2022-07-14 | Lime engineering team support emails: 'The CROW team was having trouble surfacing Lime vehicles on the dashboard due to the vehicle ID formats. Can you elaborate what's the issue in detail? [..] If it helps, we can set up a call to discuss the issue'
| 2022-06-14 | Lime emails: "What is the reason that there're no Lime vehicles in the Dashboard?" We respond: "The reason is that the feed was not following the data requirements: The GBFS feed had rotating IDs. If this is fixed, we'd love to hear, so we can activate the feed again."
| 2021-02-17 | We ask to inform us as soon as the feed checked and ready to test
| 2021-02-10 | Lime emails: "Our understanding is that we were currently sharing GBFS with CROW. We'll revert shortly with any upgraded version we may support"
| 2021-02-09 | We ask Lime to meet the specifications so that the Lime feed can be activated again
| 2021-09-14 | We ask Lime to implement static vehicle_ids
