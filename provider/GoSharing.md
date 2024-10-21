# Data quality: GO Sharing

## Data quality status

Last checked at 2024-10-21.

| **Quality check**           | **Quality**
| --                          | --
| Uses data standard?         | ✅ MDS
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ✅
| Offers service areas        | ❌

Status: 🟢 Perfect

## Improvements to make

None that we know of at the moment. GO Sharing could offer a [GBFS feed with the service areas](https://docs.dashboarddeelmobiliteit.nl/data_feeds/service_areas/) they offer.

## Logs

| Date       | Update 
| ----       | ---
| 2024-10-01 | 🐛 GEEN DATA VAN GO SHARING - De datafeed van GO Sharing wordt niet meer geactualiseerd ("Dit klopt inderdaad. Op 1 oktober is er gestart met een interne systeemintegratie. Data wordt niet meer geactualiseerd - uiteraard niet de bedoeling")
| 2022-10-14 | We analysed the both data sets and conclude that the same issue that we reported at 2022-07-26 is causing the difference in vehicles. This issue has to be fixed for an longer amount of time. We (again) send info on how to fix this and ask GO Sharing if the issue in the MDS feed can be fixed. Also we inform the municipalities that noticed the incorrect data.
| 2022-10-14 | GO Sharing sends us a spreadsheet with overview of vehicles in Tilburg, to compare with data in the Dashboard. We start comparing.
| 2022-10-10 | We share an overview of vehicles in Tilburg (data by the Dashboard Deelmobiliteit). We ask for a spreadsheet with data from GO Sharing, for the same date/time as our snapshot.
| 2022-09-19 | GO Sharing emails and mentions that the GO Sharing data team sees that the amount of vehicles in the Dashboard Deelmobiliteit and the amount in their own dashboard do not match. We mention that it might have to do with the issue we reported in 2022-07-26: Vehicles that are not in public space anymore are still given to us in the MDS feed, with the wrong vehicle status. Next to that we promise to share data for Tilburg, to compare both dashboards.
| 2022-09-19 | The Hague mentions that the amount of GO Sharing vehicles is not correct. We contact GO Sharing.
| 2022-09-15 | During the CROW Kenniscafe of September 15th we heard from Tilburg that the amount of GO Sharing vehicles didn't match the real amount of vehicles in public space. We will investigate this.
| 2022-08-24 | GO Sharing emails us and mentions that the data in the Dashboard doesn't match the data in the GO Sharing dashboard fully. Sometimes GO Sharing vehicles are standing parked for a long time in the Dashboard, while in reality the vehicle has been rented out again already. We are going to do research on this ([related](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/issues/32))
| 2022-08-17 | We email GO Sharing and ask for a status update on the incorrect feed PROW. goUrban will go after this (vehicles in depots should not be present in the data feed).
| 2022-07-26 | We notice that the feed doesn't follow the MDS PROW rules. We email GO Sharing and ask: Can you make sure that the feed only include vehicles that are in public space? We updated the GO Sharing data quality from 🟢 _Perfect_ to 🟡 _Usable though needs improvement_.
| 2022-07-10 | 🎉 We enabled the https://platform.api.gourban.services/v1/greenmo/api/mds/netherlands/vehicles MDS feed. We did disable https://greenmo.core.gourban-mobility.com/api/gbfs/en/free-bike-status GBFS feed.
| 2022-07-05 | GO Sharing emails: End of July the update for faster reponse times of the MDS /vehicles feed will be delivered.
| 2022-06-17 | We email: As goUrban is working on making the feed faster and this will be finished in the next sprint, we decided we can activate the MDS feed now. We will activate the MDS feed and inform you if this is done.

For full log history going back to 2021, see [history](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/38ea1d0b48c7dfe2fa3298e43ceac50d11a27603/provider/GoSharing.md#logs).
