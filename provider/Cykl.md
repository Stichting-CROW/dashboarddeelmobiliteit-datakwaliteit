# Data quality: Cykl

## Data quality status

Last updated: 2021-09-02.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ❌
| % Accuracy number of trips  | ...

Status: 🟡 Usable though needs improvement

### Explanation

- The data feed uses one of the supported standards 👍
- The feed is updated frequently 👍
- Cykl follows the data specification perfectly 👍
- Cykl offers data of all vehicles
- Cykl does not offer 'vehicle type' in their data feed yet

The current status is 'usable though needs improvement'. As soon as vehicle type is included in the datafeed, the status will be 🟢 Perfect.

## Improvements to make

### Add vehicle type & propulsion type

🆕 The operator should communicate what kind of vehicle it's reporting. 

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#vehicle-types).

See the GBFS documentation on how to include vehicle type information. [[1]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson) [[2]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)

For Cykl this means:

1. Add `vehicle_types.json` and include the `vehicle_types` Cykl offers:
  - `vehicle_type_id`: `cykl_type_1`
  - `form_factor`: `bicycle`,
  - `propulsion_type`: `human`,
  - `name`: `Cykl fiets type X`,
2. In `free_bike_status.json`, add `vehicle_type_id`

### Data quality statistics

Period: March 10th 2021 00:00 to March 21th 2021 00:00

| **Attribute**       | **Provider** |  **Deelfietsdashboard** | **Difference in %** | 
| --                  | --           |
| Number of trips     | 39762
| Aantal unique id's  | 39762

