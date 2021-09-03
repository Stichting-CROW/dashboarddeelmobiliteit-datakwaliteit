## Data quality status

Last updated at 2021-09-02.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ❔
| All NL data?                | ❌
| Includes vehicle type?      | ❌
| Accuracy number of trips    | Δ = 12%

Status: 🔴 Unusable

### Explanation

- The data feed uses one of the supported standards 👍
- The feed is updated frequently 👍
- We have to check if the data specification is followed perfectly
- BAQME delivers The Hague and is in process of offering data from The Hague ⏳
- BAQME does not offer 'vehicle type' in their data feed yet

The Dashboard Deelmobiliteit includes +12% more trips than BAQME reported for the periode of March 10th - March 20th 2021. This is not perfect, though the analysis was done for a small data set ([results data quality check](https://example.com)). We keep improving this.

The current status is 'unusable' as not all NL data is shared (The Hague is missing). This is the first thing that should be updated.

## Improvements to make

### Offer data for all vehicles in The Netherlands

The operator has created a data sheet for all vehicles in The Netherlands 👍. The only thing that is to be done is to offer the data feed in a format that the Dashboard can understand. As soon as this is done, the Dashboard includes all BAQME vehicles of both Rotterdam and The Hague.

### Add vehicle type & propulsion type

🆕 The operator should communicate what kind of vehicle it's reporting. 

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#vehicle-types).

See the GBFS documentation on how to include vehicle type information. [[1]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson) [[2]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)

For BAQME this means:

1. Add `vehicle_types.json` and include the `vehicle_types` BAQME offers:
  - `vehicle_type_id`: `baqme_type_1`
  - `form_factor`: `bike`,
  - `propulsion_type`: `electric_assist`,
  - `max_range_meters`: `X`,
  - `name`: `BAQME bakfiets type X`,
2. In `free_bike_status.json`, add `vehicle_type_id`
