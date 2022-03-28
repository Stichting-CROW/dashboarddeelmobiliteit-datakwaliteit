# Data quality: Felyx

## Data quality status

Last updated: 2022-01-24.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ❌ 300s
| Correct [PROW](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit#%E2%84%B9%EF%B8%8F-correct-prow-4)?               | ❌
| All NL data?                | ✅
| Includes vehicle type?      | ❌
| Accuracy number of trips    | Δ = -13.7% (March 2021)

Status: 🟡 Usable though needs improvement

## Improvements to make

### Update datafeed at most every 30 seconds

At the moment the data feed is updated every 300 seconds. Please make the datafeed update more frequently, at least every 30s.

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
| 2022-03-28 | We email Felyx and ask: Can you enable Zwolle and Enschede, or give a planning/timeline?
| 2022-03-24 | Municipality of Enschede asks us again if Felyx data can be visible in the CROW Dashboard.
| 2022-03-10 | Felyx thanks us for signaling and informs that it will enable Zwolle and Enschede data.
| 2022-03-08 | We see that Zwolle and Enschede data are missing, while Felyx offers vehicles in these cities. We email Felyx and ask to include all NL data including Zwolle and Enschede.
| 2022-02-08 | Felyx emails: 2) 'Updating all data every 30s is difficult. But, `is_disabled` is realtime now. And we are looking if `is_reserved` can be close to realtime as well'  3) We are going to work on improving PROW mid February, expected delivery: beginning of March
| 2022-02-04 | Felyx replied to our email of 2021-01-24: 1) is fixed! Haarlem & Den Bosch are now present in the data feed. 2) Updating every 30s is difficult because external software fleetbird/NIU only updates every 5 minutes. 3) Felyx will start fixing PROW
| 2022-01-27 | At +- 9:10am the new Dashboard Deelmobiliteit was launched! We ended the rental of a Felyx bike in Amsterdam, but this bike did not show up immediately on the map. What did show up nearby the location: A Felyx scooter at 7:43am and 9:22am. Maybe it was one of these, presumably the last one. If so, it had a delay of 8 minutes.
| 2022-01-27 | At 8:00 am we noticed the update frequency was reverted(?) to 5 minutes
| 2022-01-26 | At 5:13pm we noticed the update frequency was +- 30 seconds
| 2022-01-24 | We asked Felyx by mail to 1) add Haarlem and Den Bosch 2) Update update frequency to <= 30s 3) Fix PROW
| 2022-01-24 | We asked Felyx by phone to update feed frequency from 5 minutes to every 30 seconds
| 2021-09-13 | Asked Felyx to update feed frequency, add data of Den Bosch+Haarlem, fix PROW and add vehicle type
