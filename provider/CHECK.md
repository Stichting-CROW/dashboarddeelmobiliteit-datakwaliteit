# Data quality: CHECK

## Data quality status

Last checked at 2025-10-19.

| **Quality check**      | **Quality** |
| ---------------------- | ----------- |
| Uses data standard?    | ✅ MDS 2.0  |
| Updated <= 30s?        | ✅          |
| Correct PROW?          | ❌          |
| All NL data?           | ❌          |
| Includes vehicle type? | ✅          |
| Offers service areas   | ✅          |

Status: 🟡 Needs improvements

## Improvements to make

- Share data of e-bikes as well (for Amersfoort)
- Make sure there are no duplicate vehicle-ids in the feed

## Logs

| Updated    | Description                                                                                                                                                                                                                                                                                                                                                                                                    |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2025-09-01 | 🐛 Check start met het aanbieden van deelfietsen in Amersfoort, deze data wordt niet aangeleverd in de feeds.                                                                                                                                                                                                                                                                                                  |
| 2025-06-20 | 🐛 Sommige voertuig ID's zitten dubbel in de feed van check, dit zorgt soms voor incorrecte data                                                                                                                                                                                                                                                                                                               |
| 2025-06-19 | 🎉 Data feed is binnen 10 minuten na constatering van de uitval weer actief gezet door CHECK                                                                                                                                                                                                                                                                                                                   |
| 2025-06-19 | 🎉 Data feed is binnen 10 minuten na constatering van de uitval weer actief gezet door CHECK                                                                                                                                                                                                                                                                                                                   |
| 2025-06-17 | 🐛 Data feed is uitgevallen op dinsdag 17 juni 2025                                                                                                                                                                                                                                                                                                                                                            |
| 2024-08-21 | 🎉 **VERHURINGEN KLOPPEN PER VANDAAG WEER** - Per vandaag wordt de MDS-feed gebruikt in plaats van de oude GBFS-feed                                                                                                                                                                                                                                                                                           |
| 2024-08-16 | Per vandaag testen we CHECK's nieuwe MDS-feed onder de naam 'check_mdsv2'                                                                                                                                                                                                                                                                                                                                      |
| 2024-04-17 | CHECK geeft aan te willen overstappen op MDS voor voertuigmonitoring                                                                                                                                                                                                                                                                                                                                           |
| 2024-04-01 | 🐛 **VERHURINGEN ZIJN PER VANDAAG ONJUIST** - Er zijn wekelijks 20k-40k verhuringen zonder eindtijd. Oorzaak is dat CHECK de GBFS heeft veranderd en voertuig-IDs nu continu roteren. De datafeed is daarmee onbruikbaar geworden voor het Dashboard Deelmobiliteit, voor wat betreft verhuringen. Tussen april en augustus 2024 zijn hierdoor vele foutieve verhuring-records in de database terecht gekomen. |
