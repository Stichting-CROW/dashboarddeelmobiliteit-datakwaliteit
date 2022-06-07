# Data quality: GO Sharing

## Data quality status

Last updated: 2022-06-07.

| **Quality check**            | **Quality**
| --                          | --      |
| Uses data standard?         | ❌ GBFS <br><sub><sup>rotated
| Updated <= 30s?             | :heavy_check_mark:
| Correct PROW?               | :heavy_check_mark:
| All NL data?                | :heavy_check_mark:
| Includes vehicle type?      | ❌
| Accuracy number of trips    | Δ = -0,523% 👍 (last test: March 2021)

Status: 🟡 Usable though needs improvement

## Improvements to make

GO Sharing offers a new MDS feed. If the feed response does load consistently in 10 seconds or less, the feed is ready to use.

## Logs

| ----       | ---
| 2022-06-07 | GO Sharing emails: 'As promised our colleagues are busy with investigating the response time. They've tested the feed: the average response time is 6.7 seconds. It only sometimes happens that the response time is > 10 seconds. Their question is: Why keep the limit on 10 seconds, if increasing the response time limit to 15 seconds would make our feed work?' We respond: 'We keep the limit to 10 seconds because we want to prevent to have this conversation again, if in a few months the feed will be slower because of increased amount of vehicles and trips. We like to have it solved for the long-term. The old (https://greenmo.core.gourban-mobility.com/api/gbfs/en/free-bike-status) does respond in <2s, so it's unclear why the new MDS would be so much slower in response time.'
| 2022-05-23 | GO Sharing emails: 'The last change that is needed for succesful MDS integration (fast response time) can only be finalised if we know the implementation costs for this change. We will inform the municipalities on the status, on what we have done so far and what we still need to finalise the MDS feed.'
| 2022-05-17 | GO Sharing emails and mentions: "The response times will be focused on in the upcoming sprint." -> We reply that we need to get the response times right before we can activate the feed. So we don't activate the new MDS feed yet.
| 2022-05-11 | GO Sharing emails and summarizes: "Everything looks good, but the response times are a last hurdle. These response times have to be < 3 seconds to work properly."
| 2022-05-06 | GO Sharing updates us on the issue of slow response times: "Please advise on limiting the amount of data and the scope of this data, with the intent to speed the process up. We are unfortunately not considering implementing pre-cashing."
| 2022-05-03 | GO Sharing replies to our feedback sent on 2022-04-25.<br /><br />1. There are 1200 vehicles without an ID -> "The device_id is based on the IoT module ID. If the vehicle doesn't have an IoT module, this ID is null. => Those vehicles will not be provided on the MDS feed as they are most probably not deployed (without IoT)." -> Perfect!<br /><br />2. There are 800 vehicles that do not have a last_vehicle_state -> "Vehicles newly added to the system which have not gotten an update yet, could show up with these values not set. We have introduced fallback values to cover in these scenarios and prevent issues." -> Nice<br /><br />3. gzip is preferred -> "gzip has been enabled on all MDS endpoints" -> 👌<br /><br />4. Feed response time is too long --> "Regarding the processing times, they are most likely that long because you looking at the feeds of the whole fleet. If you wish we could provide you with more limited fleets looking at specific regions or cities to speed up the processing times." -> "It should be possible to speed up the endpoint to < 3-5s response times. [Here a few suggestions]. Currently we use a maximum response time of 10s in our systems (because other realtime processes depend on it). With this endpoint it sometimes goes well but sometimes it's too slow and then the import is not working. Please again have a look into this, with our suggestions in mind."
| 2022-04-25 | On April 11th 2022 the server of Dashboard Deelmobiliteit was [disabled](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/year-overview/2022.md#general-comments) for 20 minutes. Because GO Sharing doesn't use static vehicle IDs, we had to 'reset' the GO Sharing state to make sure parking events would be stored well after being offline.<br /><br />We executed the following query to fix the data: `UPDATE park_events SET end_time = '2022-04-11T15:00:00' WHERE 1=1 AND system_id = 'gosharing' AND end_time IS NULL AND start_time <= '2022-04-11T15:00:00';` With this all parking sessions on or before April 11th 2022 are ended manually (10103 entries modified).
| 2022-04-23 | We noticed 2 problems with the MDS feed: 1. There are 1200 vehicles without a device_id. 2. There are 800 vehicles that do not have a last_vehicle_state. On 2022-04-25 we email goUrban these issues with information how to fix.
| 2022-04-23 | We activated the MDS feed using the name "gosharing-mds". From now we'll run the MDS and GBFS feed in parallel. If the MDS works well for a week, we will replace the current GBFS feed with the MDS feed.
| 2022-04-20 | goUrban emails: 'Task 2 and 3 are completed'. We tested this. The MDS feed is now following the standard. We can start testing the GO Sharing MDS feed
| 2022-04-07 | 
| 2022-04-07 | goUrban answers per email: 'For 1, 2 and 3 we have created internal tasks that are currently being prioritized and I'll share an ETA with you as soon as there are any'
| 2022-04-05 | We tested the MDS feed and reply with feedback: 1. Enable gzip 2. Use correct casting for vehicle_type, propulsion_types, last_vehicle_state and last_event_types, as described in the MDS standard.
| 2022-04-05 | goUrban replies on our two questions. Regarding 2: goUrban has put the request for a token that is valid indefinately on the backlog, without ETA. Regarding 1: The documentation was not complete. We can use a request like the following to get the vehicles data: `curl "https://greenmo.core.gourban-mobility.com/api/mds/netherlands/vehicles" -H 'Authorization: Bearer THE_TOKEN' -H 'Accept: application/vnd.mds.provider+json;version=1.2.0'`
| 2022-04-04 | We tested this: getting an access token and refresh token works, though we can't get a useful response from the `https://greenmo.core.gourban.services/api/mds/netherlands/vehicles` end point. As a response we get: `{"error": "0012","error_description": "HttpMediaTypeNotAcceptable [uri=/api/mds/netherlands/vehicles]"}`. We email support@gourban.co directly (CC GO Sharing) and ask: 1) How to get the /vehicles response data? 2) Can we have a bearer token that is valid indefinitely?
| 2022-04-04 | GO Sharing emails: 'We got back form goUrban:<br /><br />"`curl --location --request POST 'https://user.api.gourban.services/v1/greenmo/auth/sign-in-api-client' --header 'Content-Type: application/json' --data-raw '{"clientId": "THE_CLIENT_ID", "clientKey": "THE_CLIENT_KEY" }'` Below you can find latest MDS doc: https://whimsical.com/mds-TCV59ZqTb2Rxo8JhB2ztiN" Do you have all the info you need with this?'
| 2022-04-01 | Gemeente Almere emails: "Vandaag is GO Sharing gestart in onze stad"
| 2022-03-28 | We ask again to share info on how to use the MDS API. We would like to receive an example cURL command.
| 2022-03-24 | We test the MDS feed based on the documentation we got. We can't get any data. We ask GO Sharing / goUrban two things: 1. Can we authenticate with a bearer token that is always valid, instead of using refreshed tokens all the time? 2. Please share example cURL commands for retrieving the vehicles data.
| 2022-03-23 | GO Sharing calls us and asks if the documentation is complete now.
| 2022-03-22 | GO Sharing sends an documentation URL, https://whimsical.com/api-basics-RPfVazKR6gTaECRG6MGnFv.
| 2022-03-22 | We tested the MDS URL, but are missing additional documentation to actually receive any data. We ask for documentation.
| 2022-03-17 | GO Sharing sents an MDS URL (https://greenmo.core.gourban-mobility.com/api/mds/netherlands/) and authentication credentials. We will test these.
| 2022-03-14 | We inform municipalities of Eindhoven, Enschede, Rotterdam and The Hague that we didn't receive an update and don't know if we will receive any updates
| 2022-03-11 | We ask what is the status of the MDS feed, as we didn't receive an update yet.
| 2022-02-14 | GO Sharing emails that it will offer a MDS feed in the new future. **This MDS feed will be ready to test on March 4th**. Municipalities will be informed that the MDS feed is ready on March 11th. Bikes and mopeds will be included (for cars GO Sharing works with an external partner, cars are on private ground)
| 2022-02-04 | GO Sharing emails: An 'action plan' has been created. The external development team now does a feasibility test. The external development will do a follow up in the beginning of week 6, 2022 (week of February 7th). As soon as this response is received, all actors involved (municipalities, CROW) will get a follow up.
| 2022-02-03 | Still no working feed having static ID's. The feed is broken since 2021-10-06, more than half a year now. We ask what the 'action plan' is that fixed this, and what will be the planning.
| 2022-01-21 | Discussed possible solutions, discussed the difference between MDS and GBFS. GO Sharing will think about a solution. 
| 2022-01-19 | We clarified that we need 1 feed for NL, as we can not load both Eindhoven _and_ NL including Eindhoven
| 2022-01-19 | GO Sharing notifies us that Eindhoven did not see the updated feed
| 2022-01-18 | Gemeente Eindhoven asks if feed inaccuracies are solved (no)
| 2022-01-17 | Gemeente Rotterdam asks if feed inaccuracies are solved (no)
| 2022-01-12 | Asked if there's 1 GBFS end point for all of The Netherlands. We can not read both the feed with all NL data (including Eindhoven) and the new Eindhoven feed, as it would result in duplicate data
| 2022-01-11 | GO Sharing shares 3 new GBFS URLs for Eindhoven, Rotterdam, Antwerp. It uses the latest GBFS standard and includes the vehicle types. Therefor it should fix "Uses data standard" and "Includes vehicle type"
| 2021-12-22 | Asked GO Sharing for a status update
| 2021-11-24 | GO Sharing will take action on the feed inaccuracies. Goal: static vehicle IDs, correct vehicle types, correct PROW
| 2021-11-08 | Asked GO Sharing to offer static IDs in the GBFS feed, OR offer an MDS feed. Asked GO Sharing to specify the right vehicle type (at this moment every vehicle is listed as a 'moped', even the e-bikes)
| 2021-10-14 | Activated new GBFS feed.<br /><br />goUrban updated their GBFS feed to the latest version 2.2 which resulted in the updated URLs. The main URL https://greenmo.core.gourban-mobility.com/api/gbfs is where all other supported endpoints can be found, according to the GBFS standard.<br /><br />NOTE: Vehicles now have rotating vehicle-IDs. This results in parking data being valid, but trip data is not. To meet the CROW Dashboard requirements, vehicle-IDs should be static
| 2021-10-13 | Got new GBFS feed URL via GO Sharing via goUrban
| 2021-10-11 | Asked GO Sharing to fix broken GBFS feed again (phone) -> GO Sharing is taking action
| 2021-10-07 | Asked GO Sharing to fix broken GBFS feed (phone + WhatsApp) -> GO Sharing made a ticket
| 2021-10-06 | Feed GO Sharing is broken: Authorisation key isn't valid
| 2021-09-13 | Asked GO Sharing to fix PROW and add vehicle type
