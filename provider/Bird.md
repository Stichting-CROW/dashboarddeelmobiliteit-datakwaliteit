# Data quality: Bird

## Data quality status

Last updated at 2022-05-19.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ MDS
| Updated <= 30s?             | ✅
| Correct PROW?               | ❔
| All NL data?                | ❌
| Includes vehicle type?      | ✅

Status: 🟢 Perfect

## Logs

| Updated    | Description
| ----       | ---
| 2022-06-07 | We tested the new Groningen and Amersfoort feed URLs. Groningen works, Amersfoort does not. We ask Bird for some support on this.
| 2022-05-27 | Bird mails: In the past you used https://mds.bird.co/vehicles. From now we ask you to use different URLs: Groningen: https://mds.bird.co/groningen/vehicles and https://mds.bird.co/amersfoort/vehicles. We updated the authentication in such a way that you can use the same authorization token for every city.
| 2022-05-20 | Bird mails: We'll check this internally and see if we can offer all vehicles data for Amersfoort in the feed. We'll come back on this soon.
| 2022-05-19 | Bird asks: Is it correct that there are no Amersfoort vehicles in the MDS feed? We reply: Yes, this is correct, only Groningen vehicles are in the MDS feed.
| 2022-04-11 | Since today Bird shares data of **Groningen** with the CROW Dashboard using MDS
| 2022-04-07 | Bird emails: 'Because of a request of the municipality of Groningen, we have given you access to the Groningen data'
| 2022-03-29 | Bird replies: "From a data-perspective, this is expected behavior. In our spec at the moment we don't include vehicles in an unknown state. Vehicles like these would fall under the state of low battery or need maintenance, and these would be classified under a status of "Maybe PROW", which we don't include in our spec for vehicle counts." "Per the MDS spec, the vehicles will go unknown when they have been inactive for 7 days. 'Unknown' vehicles are not included in the vehicle count. Before transitioning into 'Unknown' state, vehicles that are low battery will be considered 'Non-Operational' in the MDS spec - these also would not be included in vehicle count. Let us know if that works for you."
| 2022-03-28 | We reply that empty batteries shouldn’t result in the disappearance of vehicles in the /vehicles in the /vehicles endpoint, because as long the vehicle is in the PROW (public right of way) it [should](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/provider/README.md#vehicles) be in the feed. We ask: 'Can you investigate this further?'
| 2022-03-28 | Bird emails that this is the right amount of active vehicles in Amersfoort: the logistic partner had issues in Amersfoort with replacing the batteries.
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
