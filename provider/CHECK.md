# Data quality: CHECK

## Data quality status

Last checked at 2025-10-30.

| **Quality check**      | **Quality** |
| ---------------------- | ----------- |
| Uses data standard?    | ✅ MDS 2.0  |
| Updated <= 30s?        | ✅          |
| Correct PROW?          | ✅          |
| All NL data?           | ❌          |
| Includes vehicle type? | ✅          |
| Offers service areas   | ✅          |

Status: 🟡 Needs improvements

## Improvements to make

- Share data of e-bikes as well (for Amersfoort)

## Logs

| Updated    | Description                                                                                                                                                                                                                                                                                                                                                                                                    |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2025-10-27 | 🎉 De problemen van 20 juni zijn verholpen: voertuig-ID's zitten niet meer dubbel in de feed |
| 2025-09-01 | 🐛 Check start met het aanbieden van deelfietsen in Amersfoort, deze data wordt echter nog niet aangeleverd in de feeds                                                                                                                                                                                                                                                                                                  |
| 2025-06-20 | 🐛 Sommige voertuig-ID's zitten dubbel in de feed van Check, dit zorgt soms voor incorrecte data                                                                                                                                                                                                                                                                                                               |
| 2025-06-19 | 🎉 Data feed is binnen 10 minuten na constatering van de uitval weer actief gezet door Check                                                                                                                                                                                                                                                                                                                   |
| 2025-06-17 | 🐛 Data feed is uitgevallen op dinsdag 17 juni 2025                                                                                                                                                                                                                                                                                                                                                            |
| 2024-08-21 | 🎉 Verhuringen kloppen per vandaag weer. Per vandaag wordt de MDS-feed gebruikt in plaats van de oude GBFS-feed                                                                                                                                                                                                                                                                                           |
| 2024-08-16 | Per vandaag testen we Check's nieuwe MDS-feed onder de naam 'check_mdsv2'                                                                                                                                                                                                                                                                                                                                      |
| 2024-04-17 | Check geeft aan te willen overstappen op MDS voor voertuigmonitoring                                                                                                                                                                                                                                                                                                                                           |
| 2024-04-01 | 🐛 Verhuringen zijn per vandaag onjuist. Er zijn wekelijks 20k-40k verhuringen zonder eindtijd. Oorzaak is dat CHECK de GBFS heeft veranderd en voertuig-IDs nu continu roteren. De datafeed is daarmee onbruikbaar geworden voor het Dashboard Deelmobiliteit, voor wat betreft verhuringen. Tussen april en augustus 2024 zijn hierdoor vele foutieve verhuring-records in de database terecht gekomen. |
