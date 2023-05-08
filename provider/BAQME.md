# Data quality: BAQME

## Data quality status

Last check: 2023-05-08.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ❌

Status: 🟡 Usable though needs improvement

## Improvements to make

### Add vehicle type to the GBFS data feed

🆕 The operator should communicate what kind of vehicle it's reporting. 

Since GBFS 2.1 there's a field, `vehicle_type_id`, that defines what kind of vehicle is offered.

Please start offering vehicle type in the feed, following the GBFS' standard.

To do this, you can use these documentation pages: 

1. Add [vehicle_types.json](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)
2. In free_bike_status.json, add property [vehicle_type_id](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson)

As values you can use the [latest](https://github.com/NABSA/gbfs/pull/370) standard definition for electric cargo bikes:

- form_factor: `cargo_bicycle`
- propulsion_type: `electric_assist`
- max_range_meters: `X1`
- wheel_count: `2`
- max_permitted_speed: `X3`
- rated_power: `X4`

To see an example, see page 2 of [this document](https://docs.google.com/document/d/1P_oDBnFvr9qzo0_5YbnrCDYptFQV9ZUOJGfi8ACD1GE/edit#).

Thank you!

## Logs

| Updated    | Description
| ----       | ---
| 2023-03-07 | ✅ The data outage is fixed at 17:32 today. There're new, seperate GBFS feeds instead of 1 combined feed: https://baqmefleet.com/generate_full_feed.php?fleet=rtm and https://baqmefleet.com/generate_full_feed.php?fleet=dh. We prefer 1 combined feed. BAQME sais it will offer the data in 1 combined feed again.
| 2023-03-03 | 🐛 There's a data outage. We didn't receive data from the GBFS end point anymore since yesterday 8am and today. Reason was an app migration at/to Joyride.
| 2022-08-15 | BAQME emails us: 'At the moment Joyride doesn't give priority to updating the feed so it follows the GBFS standard (`is_reserved` property). We/BAQME updated our "old" custom made BAQME feed. It should give accurate data now.'
| 2022-08-15 | We didn't get any response from Joyride.
| 2022-07-19 | The Joyride GBFS feed has no rotated ID's, but it doesn't remove vehicles from the feed if these are in active rental ([though they should](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_statusjson)). We emailed Joyride and ask if they can fix the GBFS feed so it doesn't include vehicles that have an active rental.
| 2022-07-09 | We added the new GBFS feed for testing purposes.
| 2022-06-28 | BAQME asks us if we can activate the GBFS feed of joyridecity.bike, so that BAQME's can disable its own feed and save resources. 
| 2022-03-21 | BAQME emails: "We got a GBFS feed URL from our whitelabel software provider. Could you check if this feed is valid and that is does have static vehicle IDs?"
| 2022-01-31 | There has been 'fake' vehicle at [51.9103119, 4.4782139] from 2021-09-06 to 2022-01-26 11:00. Reason was: Joyride often sends this exact coordinate if there's a status change. BAQME fixed this in their feed and asked Joyride to fix it at there side as well. Since 2022-01-26 this 'fake' vehicle is not present in the data feed anymore, so all is good now
| 2021-09-09 | Asked BAQME to add vehicle type
