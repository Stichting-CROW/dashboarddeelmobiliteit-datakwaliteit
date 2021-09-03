# Data quality: Deelfiets Nederland

## Data quality status

Last updated: 2021-09-02.

| **Quality check**           | **Quality**
| --                          | -- |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ❔
| All NL data?                | ❌
| Includes vehicle type?      | ❌
| % Accuracy number of trips  | Δ = 0%

Status: 🟡 Usable though needs improvement

### Explanation

- The data feed uses one of the supported standards 👍
- The feed is updated frequently 👍
- We have to check if the data specification is followed perfectly
- Deelfiets Nederland does not offers data of all vehicles ⏳
- Deelfiets Nederland does not offer 'vehicle type' in their data feed yet

The current status is 'usable though needs improvement'. As soon as all vehicle data is included, and vehicle type is added in the datafeed, the status will be 🟢 Perfect.

## Improvements to make

### Include all vehicle data

At the moment only data of X is included. The operator should include data of all their vehicles.

### Add vehicle type & propulsion type

🆕 The operator should communicate what kind of vehicle it's reporting. 

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#vehicle-types).

See the GBFS documentation on how to include vehicle type information. [[1]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson) [[2]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)

For Deelfiets Nederland this means:

1. Add `vehicle_types.json` and include the `vehicle_types` Deelfiets Nederland offers:
  - `vehicle_type_id`: `deelfietsnederland_type_1`
  - `form_factor`: `bicycle`,
  - `propulsion_type`: `human`,
  - `name`: `Deelfiets Nederland fiets type X`,
2. In `free_bike_status.json`, add `vehicle_type_id`
