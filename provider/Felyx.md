# Data quality: Felyx

## Data quality status

Last checked at 2024-08-22.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ MDS 1.2
| Updated <= 30s?             | ❌ 300s
| Correct [PROW](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit#%E2%84%B9%EF%B8%8F-correct-prow-4)?               | ❌
| All NL data?                | ✅
| Includes vehicle type?      | ❌
| Offers service areas        | ❌

Status: 🟡 Usable though needs improvement

## Improvements to make

### Update datafeed at most every 30 seconds

? At the moment the data feed is updated every 300 seconds. Please make the datafeed update more frequently, at least every 30s.

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
| 2024-09-09 | Gemeente Den Haag meldt dat het aantal verhuringen sinds 21 augustus ineens een stuk lager is dan eerder. Felyx geeft aan dat er sinds de overgang inderdaad iets mis is in hun nieuwe datafeed, waardoor het aantal trips niet klopt. Felyx werkt aan een oplossing.
| 2024-08-21 | Per vandaag wordt de MDS-feed gebruikt in plaats van de oude GBFS-feed
| 2024-07-04 | Felyx is gestart met aanbieden van voertuigen in Hilversum
| 2024-07-04 | We hebben de voertuigdata van Felyx vergeleken met die van het Dashboard Deelmobiliteit, voor 29 juni t/m 1 juli. Elke dag kwam het aantal voertuigen in het Dashboard Deelmobiliteit en in het Felyx dashboard precies overeen, specifiek voor gemeente Zwolle. De datakwaliteit is hier dus perfect op orde.
| 2022-10-18 | Municipality of The Hague emails Felyx and asks: Can you update the feed so it shared data every 30 seconds instead of 5 minutes? The Hague needs this for the micro hubs functionality
| 2022-09-12 | Felyx does share Tilburg data with Dashboard Deelmobiliteit again. We are missing Tilburg Felyx data from September 8th until 12th
| 2022-09-08 | Felyx doesn't share Tilburg data anymore. We contacted Felyx
| 2022-05-19 | Gemeente Enschede mentions that Felyx data isn't perfect: often rentals are missing. We respond and say that the cause is that Felyx only updates its data every 300 seconds instead of the 30 seconds that is in the specifications. We will contact Felyx again on this and ask for a solution, so that in the future the data feed is refreshed every 30 seconds and municipalities will have reliable data
| 2022-04-19 | Felyx attended our 'Introduction in MDS' meeting
| 2022-03-29 | Felyx emails: Enschede and Zwolle data is now shared with the CROW Dashboard. We confirm this is the case. Issue of March 8th is solved.
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
