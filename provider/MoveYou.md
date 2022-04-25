# Data quality: MoveYou

Offers vehicles for labels:

- MoveYou
- GoAbout
- Deelfietsen Zeeland

## Data quality status

Last updated at 2022-04-07.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ⏳ TOMP
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
| 2022-04-05 | We tested the TOMP feed and it works. ~~On April 8th~~ In the end of April MoveYou will do a technical update that makes responses faster than the > 10 seconds we are currently experiencing.
| 2022-04-05 | MoveYou sends documentation on their TOMP feed, as well as credentials.
| 2022-03-28 | We reply: "Good that you'll share a TOMP feed URL and token. You don't have to share all vehicles with any status, but only vehicles that are unrented in public space, see [PROW](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#general)." We ask for the expected date on which the TOMP feed and token will be shared with us.
| 2022-03-28 | MoveYou emails: "We have to do some modifications in the existing implementation. We will implement it like this: 1. We will do authentication using a JWT token and will share the login credentials. 2. We will share all vehicles having any status."
| 2022-03-08 | MoveYou emails it will share the answers internally. If questions/comments arise, MoveYou plans a call with us.
| 2022-03-07 | We reply to the questions asked by MoveYou.
| 2022-03-07 | MoveYou emails: "As said before, we will refactor infrastructure end of 2022. But for now we think we've found a solution for offering the feed already this month." MoveYou asks 4 technical questions related to offering a TOMP feed.
| 2022-02-25 | We email: 'What makes implementing the MDS /vehicles end point complex for you? In our experience it is easy to implement'
| 2022-02-24 | MoveYou replies to our email: 'This is on our roadmap, we want to include this in our new Bike API -> Q3-Q4 2022. For the short term we cannot offer a feed, for long term we want to offer a MDS/GBFS/TOMP feed, preferable via the Bike API'
| 2022-02-17 | We ask MoveYou: can you offer a MDS/GBFS/TOMP feed as in our [specs](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/)?
| 2022-02-17 | Province of Zeeland asks to include GoAbout for Vlissingen en Middelburg, because this is a requirement for participation in the Dutch national pilot "deelfietsen op treinstations". Deelfietsen Zeeland uses GoAbout bikes that are offered by MoveYou. NS Station Vlissingen is part of the pilot.
| 2022-02-03 | MoveYou/GoAbout emails: MoveYou has acquired GoAbout and will keep operating using the GoAbout brand. MoveYou already has a GBFS and TOMP feed, though having dynamic ID's. MoveYou will check if static IDs can be offered. Otherwise it will be added to the backlog
| 2022-02-02 | We asked MoveYou/GoAbout to offer a data feed
| 2022-01-24 | Created MoveYou/GoAbout status page
