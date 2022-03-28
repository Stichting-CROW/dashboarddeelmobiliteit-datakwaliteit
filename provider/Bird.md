# Data quality: Bird

## Data quality status

Last updated at 2022-03-28.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ MDS
| Updated <= 30s?             | ✅
| Correct PROW?               | ❔
| All NL data?                | ✅
| Includes vehicle type?      | ✅

Status: 🟢 Perfect

## Logs

| Updated    | Description
| ----       | ---
| 2022-03-28 | We email Bird: "We notice that the Bird MDS feed again returns only 6 vehicles in Amersfoort, while we expect there should be more available vehicles. Could you check if the amount of vehicles that is shared by the MDS feed is correct? [additional info]"
| 2022-03-17 | We reply: "At this moment it seems to be working again. The API was working but we only got a few vehicles instead of all vehicles within Amersfoort"
| 2022-03-14 | Bird replies: "Could you provide more information here on what you're seeing on your end? Which endpoints and parameters are you looking at?"
| 2022-03-11 | We ask Bird why no vehicles are available anymore since beginning of March ([issue](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/issues/20)).
| 2022-02-21 | We've tested and activated the Bird MDS feed 🎉
| 2022-01-25 | Bird sent us the MDS end point: https://mds.bird.co/vehicles - we will test the data feed
| 2022-01-25 | We got information on logging in at https://amersfoort.open.bird.co/login. We ask: what is the URL of the MDS end point?
| 2022-01-24 | We ask if there's an update
| 2022-01-17 | Bird emails: will check development team if delivering the MDS/GBFS/TOMP feed is possible
| 2022-01-17 | Bird emails documentation of a Bird-specific API. We don't support the Bird-specific API, so we ask to share one of the [supported international data standards](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/)
| 2022-01-13 | Bird emails: Gemeente Amersfoort asked to include Bird in the Dashboard Deelmobiliteit. Bird will share their MDS/GBFS feed with us if we share an email address to share it with
