# Data quality: Lime

## Data quality status

Last updated at 2022-06-14.

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

At the moment LIME uses rotated IDs. LIME should use static IDs instead. At the moment the feed is unusable.

## Logs

|Updated    | Description
|----       | ---
|2022-06-14 | LIME emails: "What is the reason that there're no LIME vehicles in the Dashboard?" We respond: "The reason is that the feed was not following the data requirements: The GBFS feed had rotating IDs. If this is fixed, we'd love to hear, so we can activate the feed again."
|2021-02-17 | We ask to inform us as soon as the feed checked and ready to test
|2021-02-10 | LIME emails: "Our understanding is that we were currently sharing GBFS with CROW. We'll revert shortly with any upgraded version we may support"
|2021-02-09 | We ask LIME to meet the specifications so that the LIME feed can be activated again
|2021-09-14 | Asked Lime to implement static vehicle_ids
