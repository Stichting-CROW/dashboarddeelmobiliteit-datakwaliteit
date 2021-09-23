# Data quality: BAQME

## Data quality status

Last updated: 2021-09-09.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ❌
| Accuracy number of trips    | Δ = 12%

Status: 🟡 Usable though needs improvement

### Explanation

- The data feed uses one of the supported standards 👍
- The feed is updated frequently 👍
- BAQME does not offer 'vehicle type' in their data feed yet

The Dashboard Deelmobiliteit includes +12% more trips than BAQME reported for the periode of March 10th - March 20th 2021. This is not perfect, though the analysis was done for a small data set. We keep improving this.

The current status is 'usable though needs improvement'. As soon as vehicle type is added, the status will be 🟢 Perfect! 

## Improvements to make

### Add vehicle type to the GBFS data feed

🆕 The operator should communicate what kind of vehicle it's reporting. 

Since GBFS 2.1 there's a field, `vehicle_type_id`, that defines what kind of vehicle is offered.

Please start offering vehicle type in the feed, following the GBFS' standard.

To do this, you can use these documentation pages: 

1. Add [vehicle_types.json](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)
2. In free_bike_status.json, add property [vehicle_type_id](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson)

As values you can use the [latest](https://github.com/NABSA/gbfs/pull/370) standard definition for electric cargo bikes:

- form_factor: `cargo_bicycle`
- propulsion_type: `electric_assist`
- max_range_meters: `X1`
- wheel_count: `2`
- max_permitted_speed: `X3`
- rated_power: `X4`

To see an example, see page 2 of [this document](https://docs.google.com/document/d/1P_oDBnFvr9qzo0_5YbnrCDYptFQV9ZUOJGfi8ACD1GE/edit#).

Thank you!

## Logs

| Updated    | Description
| ----       | ---
| 2021-09-09 | Asked BAQME to add vehicle type
