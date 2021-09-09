# Data quality: Felyx

## Data quality status

Last updated: 2021-09-02.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ❌ 300s
| Correct PROW?               | ❌
| All NL data?                | ❌
| Includes vehicle type?      | ❌
| Accuracy number of trips    | ...

Status: 🟡 Usable though needs improvement

## Improvements to make

### Update datafeed at most every 30 seconds

At the moment the data feed is updated every 300 seconds. Please make the datafeed update more frequently, at least every 30s.

### Do include the cities Den Bosch and Haarlem

At the moment all cities are included in the data feed, apart from Den Bosch and Haarlem.

@Felyx Please include Haarlem and Den Bosch in the data feed as well.

### Don't include bikes that do not exist in public space

Felyx shares bikes with the Dashboard Deelmobiliteit that do not exist in public space.

Properties of this type of data are that it has a GPS location in public space, the property `is_disabled` is `1` and if you walk to the bike in real life, the bike is not there.

To see examples of this type of incorrect data, [see this document](./Felyx_extra.md).

### Add vehicle type & propulsion type

🆕 The operator should communicate what kind of vehicle it's reporting. 

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#vehicle-types).

See the GBFS documentation on how to include vehicle type information. [[1]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson) [[2]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)

For Felyx this means:

1. Add `vehicle_types.json` and include the `vehicle_types` Felyx offers:
  - `vehicle_type_id`: `felyx_type_1`
  - `form_factor`: `scooter`,
  - `propulsion_type`: `electric`,
  - `max_range_meters`: `X`,
  - `name`: `Felyx scooter type X`,
2. In `free_bike_status.json`, add `vehicle_type_id`
