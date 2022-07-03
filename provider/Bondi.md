# Data quality: Bondi

## Data quality status

Last updated at 2022-07-03.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ⏳ MDS
| Updated <= 30s?             | ➖
| Correct PROW?               | ➖
| All NL data?                | ➖
| Includes vehicle type?      | ➖

Status: 🔴 Unusable

## Improvements to make

### Offer data feed

At this moment Bondi does not yet offer a data feed.

## Logs

| Updated    | Description
| ----       | ---
| 2022-06-30 | wunder mobility answers: 'I've opened a change request to our product team to evaluate a change on that and let you know about our decision.'
| 2022-06-30 | The feed works. Although all vehicles are split up in batches of 20. We ask: 'It would be really nice for us to not use pagination. Paging would add a lot of latency. Is there a possibility to setup a higher limit so that we can retreive all the vehicles instead of only 20 per api call?'
| 2022-06-30 | wunder mobility emails the https://bondi.backend.fleetbird.eu/rest/mds/v1/vehicles end point and shares the access token.
| 2022-06-23 | wunder mobility emails: 'We support MDS v0 and v1, GBFS v1 and v2.2, TOMP v1.2, and also SIVU v1 (mostly used in Paris?)'
| 2022-06-23 | Bondi emails: 'We have switched to our new app. I link you to my contact at wunder mobility to integrate with CROW Dashboard further'
| 2022-05-16 | We email the contact person at wunder mobility and ask if a feed can be offered.
| 2022-04-26 | Bondi replies and connects us to a contact person at wunder mobility. 
| 2022-04-25 | We email Bondi: 'Can we help with getting Bondi into the CROW Dashboard? We could help testing a data feed offered by wunder mobility?'
| 2022-03-23 | Gemeente Den Haag asks: "Bondi switches to [wunder mobility](https://www.wundermobility.com/) in June. Can wunder mobility offer a feed so Bondi can integrate with CROW Dashboard?"
| 2022-02-02 | Bondi emails: "I received some info from our software provider. The current version of MDS doesn't support the /vehicles endpoints. They expect to upgrade the MDS feed in Q2. I will keep you updated when there are any changes". We reply that MDS is prefered, but GBFS and TOMP works as well. We'll wait on Bondi's update in Q2
| 2022-01-15 | We asked for documentation on how to use the authentication key
| 2022-01-14 | Bondi sent an MDS URL and authentication key
| 2022-01-10 | Email from Bondi: 'We do not yet switch to the new app provider in the next 4 months. Until we switch we don't have a TOMP feed yet.'
| 2021-12-02 | Email from Bondi: 'We will send the TOMP feed URL as soon as it's available, presumably in January 2022.'
| 2021-10-27 | Email from Bondi: 'We are switching app providers for the 1st of Jan. The new provider (Wunder mobility) has TOMP support.' We linked the [HR data spec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/) to make sure the TOMP feed will have static IDs, like in our specification.
