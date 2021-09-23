# Data quality: CHECK

## Data quality status

Last updated: 2021-09-09.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ❌
| All NL data?                | ✅
| Includes vehicle type?      | ❌
| Accuracy number of trips    | Δ = -0.083% 👍

Status: 🟡 Usable though needs improvement

### Explanation

- The data feed uses one of the supported standards 👍
- The feed is updated frequently 👍
- CHECK doesn't follow the data specification (`is_disabled`) ⏳
- CHECK offers data of all vehicles 👍
- CHECK does not offer 'vehicle type' in their data feed yet

The current status is 'usable though needs improvement'. As soon as the [PROW](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit#%E2%84%B9%EF%B8%8F-correct-prow-4) is right and vehicle type is included in the datafeed, the status will be 🟢 Perfect.

## Improvements to make

### Don't include mopeds that do not exist in public space

CHECK shares mopeds with the Dashboard Deelmobiliteit that do not exist in public space.

Properties of this type of data are that it has a GPS location in public space, the property `is_disabled` is `true` and if you walk to the bike in real life, the moped is not there.

For an example of this type of incorrect data, see:

```json
{
  "bike_id": "e79688f8-b4ad-4cb6-8491-00e3b4802bb4",
  "is_disabled": true,
  "is_reserved": false,
  "lat": 51.908538,
  "lon": 4.445308
},
```

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
- max_permitted_speed: `X3`
- rated_power: `X4`

To see an example, see page 2 of [this document](https://docs.google.com/document/d/1P_oDBnFvr9qzo0_5YbnrCDYptFQV9ZUOJGfi8ACD1GE/edit?usp=sharing).

## Logs

| Updated    | Description
| ----       | ---
| 2021-09-10 | Sander (CHECK) informed development team on our request
| 2021-09-09 | Asked CHECK to fix PROW and add vehicle type
