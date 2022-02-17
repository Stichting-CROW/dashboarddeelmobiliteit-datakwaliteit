# Data quality: MoveYou

Offers vehicles for labels:

- MoveYou
- GoAbout
- Deelfietsen Zeeland

## Data quality status

Last updated at 2022-02-17.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ❌
| Updated <= 30s?             | ❌
| Correct PROW?               | ❌
| All NL data?                | ❌
| Includes vehicle type?      | ❌

Status: 🔴 Unusable

## Improvements to make

### Offer a data feed

Offer any of the supported data standards, preferably MDS.

## Logs

| Updated    | Description
| ----       | ---
| 2022-02-17 | We ask MoveYou: can you offer a GBFS feed as in our [specs](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/)?
| 2022-02-17 | Province of Zeeland asks to include GoAbout for Vlissingen en Middelburg, because this is a requirement for participation in the Dutch national pilot "deelfietsen op treinstations". Deelfietsen Zeeland uses GoAbout bikes that are offered by MoveYou. NS Station Vlissingen is part of the pilot.
| 2022-02-03 | MoveYou/GoAbout emails: MoveYou has acquired GoAbout and will keep operating using the GoAbout brand. MoveYou already has a GBFS and TOMP feed, though having dynamic ID's. MoveYou will check if static IDs can be offered. Otherwise it will be added to the backlog
| 2022-02-02 | We asked MoveYou/GoAbout to offer a data feed
| 2022-01-24 | Created MoveYou/GoAbout status page
