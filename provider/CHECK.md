# Data quality: CHECK

## Data quality status

Last checked at 2025-02-12.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ MDS 2.0
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ✅
| Offers service areas        | ✅

Status: 🟢 Perfect

## Improvements to make

None

## Logs

| Updated    | Description
| ----       | ---
| 2024-08-21 | 🎉 **VERHURINGEN KLOPPEN PER VANDAAG WEER** - Per vandaag wordt de MDS-feed gebruikt in plaats van de oude GBFS-feed
| 2024-08-16 | Per vandaag testen we CHECK's nieuwe MDS-feed onder de naam 'check_mdsv2'
| 2024-04-17 | CHECK geeft aan te willen overstappen op MDS voor voertuigmonitoring
| 2024-04-01 | 🐛 **VERHURINGEN ZIJN PER VANDAAG ONJUIST** - Er zijn wekelijks 20k-40k verhuringen zonder eindtijd. Oorzaak is dat CHECK de GBFS heeft veranderd en voertuig-IDs nu continu roteren. De datafeed is daarmee onbruikbaar geworden voor het Dashboard Deelmobiliteit, voor wat betreft verhuringen. Tussen april en augustus 2024 zijn hierdoor vele foutieve verhuring-records in de database terecht gekomen.
