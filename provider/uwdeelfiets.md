# Data quality: uwdeelfiets

## Data quality status

Last updated: 2021-09-02.

| **Quality check**           | **Quality**
| --                          | -- |
| Uses data standard?         | ✅ MDS
| Updated <= 30s?             | ❔
| Correct PROW?               | ❔
| All NL data?                | ❌
| Includes vehicle type?      | ❌
| % Accuracy number of trips  | ...

Status: 🔴 Unusable

## Improvements to make

### Offer NL data

At the moment uwdeelfiets only offers data from .. and ... uwdeelfiets should offer data from all of NL.

### Add vehicle type & propulsion type

🆕 The operator should communicate what kind of vehicle it's reporting. 

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#vehicle-types).

See the GBFS documentation on how to include vehicle type information. [[1]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson) [[2]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)

For uwdeelfiets this means:

1. Add `vehicle_types.json` and include the `vehicle_types` uwdeelfiets offers:
  - `vehicle_type_id`: `uwdeelfiets_type_1`
  - `form_factor`: `scooter`,
  - `propulsion_type`: `electric`,
  - `max_range_meters`: `X`,
  - `name`: `uwdeelfiets scooter type X`,
2. In `free_bike_status.json`, add `vehicle_type_id`
