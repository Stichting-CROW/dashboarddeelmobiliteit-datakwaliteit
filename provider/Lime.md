# Data quality: Lime

## Data quality status

Last updated at 2022-08-17.

| **Quality check**           | **Quality**
| --                          | --                  |
| Uses data standard?         | ❌ GBFS rotated IDs
| Updated <= 30s?             | ✅
| Correct PROW?               | ❔
| All NL data?                | ✅
| Includes vehicle type?      | ✅

Status: 🔴 Unusable

## Improvements to make

### Use static vehicle IDs

At the moment Lime uses rotated IDs. Lime should use static IDs instead. At the moment the feed is unusable.

## Logs

|Updated    | Description
|----       | ---
|2022-08-17 | We answer: "The Lime GBFS feed is disabled as it's using rotating IDs and this is not following the [data feed requirements](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/). We ask to offer a MDS `/vehicles` feed or a GBFS 1.0 `/free_bike_status.json` feed. Please offer one of these, or let us know if you have any questions."
|2022-07-14 | Lime engineering team support emails: 'The CROW team was having trouble surfacing Lime vehicles on the dashboard due to the vehicle ID formats. Can you elaborate what's the issue in detail? [..] If it helps, we can set up a call to discuss the issue'
|2022-06-14 | Lime emails: "What is the reason that there're no Lime vehicles in the Dashboard?" We respond: "The reason is that the feed was not following the data requirements: The GBFS feed had rotating IDs. If this is fixed, we'd love to hear, so we can activate the feed again."
|2021-02-17 | We ask to inform us as soon as the feed checked and ready to test
|2021-02-10 | Lime emails: "Our understanding is that we were currently sharing GBFS with CROW. We'll revert shortly with any upgraded version we may support"
|2021-02-09 | We ask Lime to meet the specifications so that the Lime feed can be activated again
|2021-09-14 | We ask Lime to implement static vehicle_ids
