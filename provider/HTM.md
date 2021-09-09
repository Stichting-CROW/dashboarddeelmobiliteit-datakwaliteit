# Data quality: HTM

## Data quality status

Last updated: 2021-09-02.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ❌
| Correct PROW?               | ❔
| All NL data?                | ❌
| Includes vehicle type?      | ❌
| % Accuracy number of trips  | ...

Status: 🔴 Unusable

## Improvements to make

### Update feed at least every 30 seconds

At the moment the GBFS feed is updated every X seconds. HTM should update the feed at least every 30 seconds.

### Offer all NL data

At the moment HTM offers only data from vehicles in X. HTM should offer data of all NL vehicles.

### Add vehicle type & propulsion type

🆕 The operator should communicate what kind of vehicle it's reporting. 

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#vehicle-types).

See the GBFS documentation on how to include vehicle type information. [[1]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson) [[2]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)

For HTM this means:

1. Add `vehicle_types.json` and include the `vehicle_types` HTM offers:
  - `vehicle_type_id`: `htm_type_1`
  - `form_factor`: `scooter`,
  - `propulsion_type`: `electric`,
  - `max_range_meters`: `X`,
  - `name`: `HTM scooter type X`,
2. In `free_bike_status.json`, add `vehicle_type_id`
