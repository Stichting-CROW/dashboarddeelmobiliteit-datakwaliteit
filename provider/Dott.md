# Data quality: Dott

## Data quality status

Last updated at 2022-04-07.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ✅

Status: 🟢 Perfect

## Improvements to make

Possible improvement:

- Offer a MDS data feed instead of a GBFS feed

## Logs

| Updated    | Description
| ----       | ---
| 2022-04-13 | We have had great chat communication with Dott, tested the GBFS feed and it all works well. For now we keep the feed disabled until Dott starts operating in The Netherlands
| 2022-04-08 | Dott emails us: "It's expected that we get an ERR_ACCESS_DENIED because no regions are currently visible aka public. We will add Amsterdam to the feed, so you can test with this data."
| 2022-04-05 | We email Dott and ask: "We tried but cannot retrieve any data. If we run the [example script](https://github.com/bartwr/dott-gbfs/blob/main/test.js) using the credentials you shared using BitWarden, we get this as a response: `{ error: 'Unauthorized: ERR_ACCESS_DENIED' }` Could you please test our credentials using the example code you've given us? Maybe it doesn't work, because we need a specific end point for every city? I hope you can point us in the right direction to get rid of the ERR_ACCESS_DENIED error."
| 2022-04-05 | We have received credentials and documentation on how to connect with Dott's GBFS feed.
| 2022-03-30 | We are in direct contact with the Engineering Manager at Dott, on how to integrate with CROW Dashboard. We communicate using a private Slack channel at Dott's Slack. We share: "For succesful integration with CROW Dashboard there should be a GBFS feed that has vehicles that keep their vehicle IDs static as long as they're in public space, or the MDS `/vehicles` end point should be offered."
| 2022-03-29 | We speak with Dott's General Manager The Netherlands by phone. Goal: finalize the integration for Amersfoort soon.
| 2022-03-29 | Dott sends extra info on the data standards they support: "For GBFS we support v2.2 and v3.0. MDS has full v0.4 implementation. MDS has a partial implementation for the Provider component at v1.2. Please note this is only partial support of full v1.2 Provider component (we only make available the Trips and Status Changes endpoints)"
| 2022-03-22 | Dott emails and aks: "Currently our implementation of MDS requires that we share credentials on a per-region basis (due to some technical constraints). For the coming launch in The Netherlands, we have several cities in scope (Apeldoorn, Zwolle, Amersfoort, Hengelo, Enschede). For each of these cities (and others to come) we would have to provide you with credentials for each city. Is this a problem for you and your organization? Do know that we will be working on building a more robust system in the future."
| 2022-02-22 | We did an introduction call. Dott will share a MDS feed soon. Dott starts to be active in The Netherlands +- March 2022
