# Data quality: TIER

## Data quality status

Last updated: 2023-07-13.

| **Quality check**           | **Quality**
| --                          | --      |
| Uses data standard?         | 🟢 MDS
| Updated <= 30s?             | ❔
| Correct PROW?               | ❔
| All NL data?                | ❔
| Includes vehicle type?      | ❔

Status: 🟢

## Improvements to make

### Bied een werkende MDS-feed aan

Per 31 mei stopte de TIER datafeed opeens met werken. TIER heeft nieuwe documentatie aangeleverd voor verbinden met de TIER MDS-feed, maar de stappen werken niet. Vanaf 26 juni kan een ontwikkelaar bij TIER ons hierbij verder helpen. Doel is een werkende MDS-feed te hebben, want zonder feed is er geen data.

## Logs

| Updated    | Description
| ----       | ---
| 2023-07-13 | Authenticatie probleem verholpen, werkende MDS /vehicles feed.
| 2023-06-19 | 🐛 TIER noemt: volgende week kan de developer hiernaar kijken (>= 26 juni)
| 2023-06-16 | 🐛 The MDS credentials work, but getting the vehicles doesn't. We ask TIER to investigate why we get an error ('cannot get length of undefined')
| 2023-06-13 | 🐛 Feed is still down. Today we got the MDS credentials.
| 2023-06-05 | 🐛 GBFS-feed is down since May 31th. Reason: "CROW DD used version 1.2. We (TIER) were accepting any version in the URL, and if the version was not not valid we simply fell back to version 2.1. From now we are only accepting major version 2 (and 3 later on)". We asked for an alternative feed, in example MDS. There is MDS ([docs](https://api-documentation.tier-services.io/docs/data-sharing/MDS/TIER%20MDS%20API%20v1.2.html)) and we'll get the credentials
| 2022-06-07 | We disabled the old feeds for the 4 NL cities, and activated the new feed. The new feed seems to work fine.
| 2022-05-30 | TIER has created a new GBFS 2.1 feed URL that we can use to get all NL data: https://platform-services.tier-services.io/data-sharing/tier_shard_south_west_europe_middle_east/gbfs/1.2/free-bike-status. In the past we had to add a new GBFS 2.2 feed for every new city that TIER started to be active in. Good news.
| 2022-04-28 | TIER has given us access to TIER data of Almere - Almere is active now
| 2022-04-23 | We email TIER and ask: "Can you give us access to the GBFS feed of Almere?"
| 2022-04-19 | We try to activate TIER Almere, but don't have access yet
| 2022-04-18 | Gemeente Almere asks to activate TIER Almere
| 2022-04-14 | Gemeente Almere mentions that TIER starts +- April 14th in Almere
| 2022-03-16 | TIER emails: "We've heard from Gemeente Amersfoort that there might be a difference between the active vehicles that we have versus the active vehicles that are visible in the CROW Dashboard. Amersfoort received a report with data from dec 2021 - feb 2022. It might be good to check if there's a difference. Or maybe you can clarify how the CROW Dashboard defines 'active vehicles' (vs how TIER sees it)"
| 2022-03-14 | TIER replies that MDS /vehicles end point is not supported indeed: "Currently, we only support MDS version 1.0.0. Available endpoints are listed on the documentation page that we have shared here previously. /vehicles was added in MDS 1.2.0. At the moment we do not support MDS version 1.2.0". Additionally TIER mentions that they'd like to know how GBFS is used by CROW Dashboard: "The original problem was that there is data inconsistency and we do not know how they calculated this. It would help a lot to understand how they plan to use GBFS and MDS to calculate things."
| 2022-03-08 | We tested the MDS end point. The credentials work, but there's no [/vehicles](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/provider/README.md#vehicles) end point that we need. We ask TIER if this MDS end point (/vehicles) is available as well. If not, we keep using GBFS as this works perfectly at the moment. 
| 2022-03-03 | TIER sends us API credentials and the MDS API documentation: https://api-documentation.tier-services.io/docs/data-sharing/Data%20Sharing%20Endpoints.html
| 2022-02-21 | We understand that there's a MDS feed as well. A MDS feed gives better data than a GBFS feed. Therefor we ask if it is possible to offer a MDS feed.
| 2022-02-17 | 🎉 We activated the new Amersfoort and Eindhoven feed
| 2022-02-09 | TIER emails GBFS feed URLs of Amersfoort and Eindhoven (and made our API key valid for using these feeds)
| 2022-02-07 | We ask to share GBFS feed URL and API key for Amersfoort and Eindhoven. We will load multiple individual feeds for now, instead of 1 feed for all of NL.
| 2022-01-24 | TIER emails and asks: 'Is it possible to process multiple seperate feeds instead of 1 feed for all places in NL?' We reply that best would be 1 feed, but for now we can do this.
| 2022-01-21 | TIER mentions that there's not 1 NL feed, but only individual feeds per city. "Providing one API link for all cities is more work and needs to be included later on the road map"
| 2022-01-10 | TIER pro-actively asks if Eindhoven and Amersfoort can be added as well. We reply: If these cities are added to to the existing GBFS (NL) feed, these are included automatically
| 2021-12-23 | 🎉 GBFS feed for TIER Utrecht is added!
| 2021-10-13 | From a legal side we are fine and can start working on the technical implementation together with CROW
