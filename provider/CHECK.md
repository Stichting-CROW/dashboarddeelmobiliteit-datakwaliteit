# Data quality: CHECK

## Data quality status

Last checked at 2022-09-05.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ❌
| All NL data?                | ✅
| Includes vehicle type?      | ❌

Status: 🟡 Usable though needs improvement

## Improvements to make

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
| 2023-01-23 | Groningen noticed the CHECK data is missing since January 17th 2AM. We see that we receive incomplete data from CHECK: Only 5 vehicles are sent to us. We ask CHECK to resolve this.
| 2022-10-07 | We investigated the issue. We were using an http end point and not a https end point. Since last week the CHECK http end point stopped working. Therefor the feed didn't work since X. This has been fixed now
| 2022-09-30 | Since today no CHECK rentals are registered anymore
| 2022-01-24 | We checked if PROW is correct at this moment. It is :)  so far we can see. Issues [[1]](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/issues/9), [[2]](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/issues/10) and [[3]](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/issues/11) were fixed. We update the quality status of PROW from ❌ to ✅
| 2021-09-10 | Sander (CHECK) informed development team on our request
| 2021-09-09 | Asked CHECK to fix PROW and add vehicle type
