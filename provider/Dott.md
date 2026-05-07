# Data quality: Dott

## Data quality status

Last checked at 2025-02-12.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ MDS 1.2
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ❌

Status: 🟢 Perfect

## Improvements to make

- Offer GBFS `/geofencing_zones` datafeed

## Logs

| Updated    | Description
| ----       | ---
| 2026-05-07 | 🎉 Per vandaag is Dott van Groningen beschikbaar in het Dashboard Deelmobiliteit
| 2024-11-04 | ✅ **DATA VAN DOTT BESCHIKBAAR** - We hebben de MDS datafeed geintegreerd; deze is nu actief (Eindhoven)
| 2024-10-30 | We hebben enkele mails over en weer verstuurd: vooralsnog biedt Dott enkel de 'variant op Oauth2 credentials grant' aan, zoals omschreven in Dott's [MDS authentication docs](https://ridedott.dev/docs/services/mds/guides/authentication/)
| 2024-10-25 | Dott heeft een MDS-feed gestuurd. Deze werkt goed zo te zien. Er is alleen een niet-gangbare manier van authenticeren. We vragen of [OAuth met client_credentials](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/general-information.md#oauth-20) gebruikt kan worden, gezien dat de door MDS aanbevolen manier van authenticeren is
| 2024-09-26 | 🐛 **GEEN DATA VAN DOTT** - TIER is nu Dott. We zullen de datafeed van Dott gaan integreren. We hebben nog geen datafeed ontvangen
| 2022-07-11 | Dott decided to stop all activities on the Dutch market. We don't get data from Dott anymore
