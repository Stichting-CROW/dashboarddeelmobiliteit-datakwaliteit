# Data quality: Lime

## Data quality status

Last checked 2022-09-09.

| **Quality check**           | **Quality**
| --                          | --                  |
| Uses data standard?         | ✅ MDS
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ✅

Status: 🟢 Perfect

## Improvements to make

None at the moment.

## Logs

| Updated    | Description
| ----       | ---
| 2022-09-09 | Lime shared the MDS feed and credentials with us. From today we re-activated Lime in the Dashboard.
| 2022-09-05 | We email Lime: Can me do a quick call to make the CROW Dashboard Deelmobiliteit integration happen? 
| 2022-08-17 | We answer: "The Lime GBFS feed is disabled as it's using rotating IDs and this is not following the [data feed requirements](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/). We ask to offer a MDS `/vehicles` feed or a GBFS 1.0 `/free_bike_status.json` feed. Please offer one of these, or let us know if you have any questions."
| 2022-07-14 | Lime engineering team support emails: 'The CROW team was having trouble surfacing Lime vehicles on the dashboard due to the vehicle ID formats. Can you elaborate what's the issue in detail? [..] If it helps, we can set up a call to discuss the issue'
| 2022-06-14 | Lime emails: "What is the reason that there're no Lime vehicles in the Dashboard?" We respond: "The reason is that the feed was not following the data requirements: The GBFS feed had rotating IDs. If this is fixed, we'd love to hear, so we can activate the feed again."
| 2021-02-17 | We ask to inform us as soon as the feed checked and ready to test
| 2021-02-10 | Lime emails: "Our understanding is that we were currently sharing GBFS with CROW. We'll revert shortly with any upgraded version we may support"
| 2021-02-09 | We ask Lime to meet the specifications so that the Lime feed can be activated again
| 2021-09-14 | We ask Lime to implement static vehicle_ids
