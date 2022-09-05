# Data quality: GO Sharing

## Data quality status

Last checked at 2022-09-05.

| **Quality check**           | **Quality**
| --                          | --
| Uses data standard?         | :heavy_check_mark: MDS
| Updated <= 30s?             | :heavy_check_mark:
| Correct PROW?               | ❌
| All NL data?                | :heavy_check_mark:
| Includes vehicle type?      | :heavy_check_mark:

Status: 🟡 Usable though needs improvement

## Improvements to make

### Remove vehicles that are in depots

Regarding the CROW Dashboard Deelmobiliteit [data feed specifications](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#general), vehicles that are not in de public space should _not_ be in the feed.

Following the MDS specifications vehicles in depots may be included in the feed for _at most_ [90 minutes](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/provider/README.md#vehicles). This is optional: you can also remove the vehicles from the feed instantly from the moment that these are outside of public space. The vehicles should only be included in the feed again, if the vehicles are in put into public space (this is called '[PROW](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/general-information.md#vehicle-states=)' in the MDS documentation).

> For the states elsewhere and removed which include vehicles not in the PROW but provide some operational clarity for agencies, these must only persist in the feed for 90 minutes before being removed.

### Improve the feed response time

Sometimes it takes 15 seconds to get a response. Pleae make sure that it's always < 10 seconds loading time.

## Logs

| Date       | Update 
| ----       | ---
| 2022-08-24 | GO Sharing emails us and mentions that the data in the Dashboard doesn't match the data in the GO Sharing dashboard fully. Sometimes GO Sharing vehicles are standing parked for a long time in the Dashboard, while in reality the vehicle has been rented out again already. We are going to do research on this ([related](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/issues/32))
| 2022-08-17 | We email GO Sharing and ask for a status update on the incorrect feed PROW. goUrban will go after this (vehicles in depots should not be present in the data feed).
| 2022-07-26 | We notice that the feed doesn't follow the MDS PROW rules. We email GO Sharing and ask: Can you make sure that the feed only include vehicles that are in public space? We updated the GO Sharing data quality from 🟢 _Perfect_ to 🟡 _Usable though needs improvement_.
| 2022-07-10 | 🎉 We enabled the https://platform.api.gourban.services/v1/greenmo/api/mds/netherlands/vehicles MDS feed. We did disable https://greenmo.core.gourban-mobility.com/api/gbfs/en/free-bike-status GBFS feed.
| 2022-07-05 | GO Sharing emails: End of July the update for faster reponse times of the MDS /vehicles feed will be delivered.
| 2022-06-17 | We email: As goUrban is working on making the feed faster and this will be finished in the next sprint, we decided we can activate the MDS feed now. We will activate the MDS feed and inform you if this is done.

For full log history going back to 2021, see [history](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/38ea1d0b48c7dfe2fa3298e43ceac50d11a27603/provider/GoSharing.md#logs).
