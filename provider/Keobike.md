# Data quality: Keobike

## Data quality status

Last updated at 2021-09-02.

| **Quality check**           | **Quality**
| --                          | --      |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ❔
| All NL data?                | ✅
| Includes vehicle type?      | ❌
| % Accuracy number of trips  | ...

Status: 🟡 Usable though needs improvement

## Improvements to make

### Add vehicle type & propulsion type

🆕 The operator should communicate what kind of vehicle it's reporting. 

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#vehicle-types).

See the GBFS documentation on how to include vehicle type information. [[1]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson) [[2]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)

For Keobike this means:

1. Add `vehicle_types.json` and include the `vehicle_types` Keobike offers:
  - `vehicle_type_id`: `keobike_type_1`
  - `form_factor`: `scooter`,
  - `propulsion_type`: `electric`,
  - `max_range_meters`: `X`,
  - `name`: `Keobike scooter type X`,
2. In `free_bike_status.json`, add `vehicle_type_id`
