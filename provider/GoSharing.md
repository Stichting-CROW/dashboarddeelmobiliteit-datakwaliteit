# Data quality: GO Sharing

## Data quality status

Last updated: 2021-09-02.

| **Quality check**            | **Quality**
| --                          | --      |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ❌
| All NL data?                | ✅
| Includes vehicle type?      | ❌
| Accuracy number of trips    | Δ = -0,523% 👍

Status: 🟡 Usable though needs improvement

## Improvements to make

### Don't include mopeds that do not exist in public space

GO Sharing shares mopeds with the Dashboard Deelmobiliteit that do not exist in public space.

Properties of this type of data are that it has a GPS location in public space, the property `is_disabled` is `1` and if you walk to the bike in real life, the moped is not there.

To see examples of this type of incorrect data, [see this document](./GoSharing_extra.md).

### Add vehicle type

🆕 The operator should communicate what kind of vehicle it's reporting. 

Since GBFS 2.1 there's a field, `vehicle_type_id`, that defines what kind of vehicle is offered.

Please start offering vehicle type in the feed, following the GBFS standard.

To to this, you can use these documentation pages: 

1. Offer [vehicle_types.json](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)
2. In free_bike_status.json, add property [vehicle_type_id](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson)

As values you can use the [latest](https://github.com/NABSA/gbfs/pull/370) standard definition for mopeds:

- form_factor: `moped`
- propulsion_type: `electric`
- max_range_meters: `X1`
- wheel_count: `2`
- max_permitted_speed *: `X3`
- rated_power: `X4`

With the `max_permitted_speed` included we can make the distinction between mopeds that are max. 45 km/h and moped with a max. speed of 25 km/h.

To see an example, see page 2 of [this document](https://docs.google.com/document/d/1P_oDBnFvr9qzo0_5YbnrCDYptFQV9ZUOJGfi8ACD1GE/edit?usp=sharing).

## Logs

| Updated    | Description
| ----       | ---
| 2021-09-13 | Asked GO Sharing to fix PROW and add vehicle type
