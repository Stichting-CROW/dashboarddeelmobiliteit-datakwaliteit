# Data quality: Felyx

## Data quality status

Last updated: 2021-09-09.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ❌ 300s
| Correct [PROW](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit#%E2%84%B9%EF%B8%8F-correct-prow-4)?               | ❌
| All NL data?                | ❌
| Includes vehicle type?      | ❌
| Accuracy number of trips    | Δ = -13.7%

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
| 2021-09-13 | Asked Felyx to update feed frequency, add data of Den Bosch+Haarlem, fix PROW and add vehicle type
