# Data quality: Donkey Republic

## Data quality status

Last updated at 2021-09-02.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ❌
| All NL data?                | ✅
| Includes vehicle type?      | ❌
| % Accuracy number of trips  | ...

Status: 🟡 Usable though needs improvement

### Explanation

- The data feed uses one of the supported standards 👍
- The feed is updated frequently 👍
- Donkey Republic doesn't follow the data specification (`is_disabled`) ⏳
- Donkey Republic offers data of all vehicles 👍
- Donkey Republic does not offer 'vehicle type' in their data feed yet

The current status is 'usable though needs improvement'. It's important that vehicles that are not in public space are not offered to the Dashboard Deelmobiliteit. Also the vehicle type should be included. After these two changes are implemented the status will be 🟢 Perfect.

## Improvements to make

### Don't include bikes that do not exist in public space

Donkey Republic shares bikes with the Dashboard Deelmobiliteit, that do not exist in public space.

Properties of this type of data is that it has a GPS location in public space, the property `is_disabled` is `1` and if you walk to the bike in real life, the bike is not there.

To see examples of this type of incorrect data, [see this document](./DonkeyRepublic_extra.md).

### Add vehicle type & propulsion type

🆕 The operator should communicate what kind of vehicle it's reporting. 

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#vehicle-types).

See the GBFS documentation on how to include vehicle type information. [[1]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson) [[2]](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)

For Donkey Republic this means:

1. Add `vehicle_types.json` and include the `vehicle_types` Donkey Republic offers:
  - Bike type 1:
    - `vehicle_type_id`: `donkeyrepublic_type_x`
    - `form_factor`: `bicycle`,
    - `propulsion_type`: `human`,
    - `name`: `Donkey Republic fiets type Y`
  - Bike type 2:
    - `vehicle_type_id`: `donkeyrepublic_type_y`
    - `form_factor`: `bicycle`,
    - `propulsion_type`: `electric`,
    - `name`: `Donkey Republic e-fiets type Y`
2. In `free_bike_status.json`, add `vehicle_type_id`
