# Data quality: GO Sharing

## Data quality status

Last updated: 2021-11-18.

| **Quality check**            | **Quality**
| --                          | --      |
| Uses data standard?         | ❌ GBFS (rotates id's)
| Updated <= 30s?             | :heavy_check_mark:
| Correct PROW?               | ❌
| All NL data?                | :heavy_check_mark:
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

To see an example, see page 2 of [this document](https://docs.google.com/document/d/1P_oDBnFvr9qzo0_5YbnrCDYptFQV9ZUOJGfi8ACD1GE/edit?usp=sharing). To choose the right vehicle type for your vehicle, see our guide: [How to offer vehicle type in GBFS](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#how-to-offer-vehicle-type-in-gbfs).

## Logs

| Updated&nbsp;&nbsp;&nbsp;&nbsp; | Description
| ----       | ---
| 2022-02-14 | GO Sharing emails that it will offer a MDS feed in the new future. This MDS feed will be ready to test on March 4th. Bikes and mopeds will be included (for cars GO Sharing works with an external partner, cars are on private ground)
| 2022-02-04 | GO Sharing emails: An 'action plan' has been created. The external development team now does a feasibility test. The external development will do a follow up in the beginning of week 6, 2022 (week of February 7th). As soon as this response is received, all actors involved (municipalities, CROW) will get a follow up.
| 2022-02-03 | Still no working feed having static ID's. The feed is broken since 2021-10-06, more than half a year now. We ask what the 'action plan' is that fixed this, and what will be the planning.
| 2022-01-21 | Discussed possible solutions, discussed the difference between MDS and GBFS. GO Sharing will think about a solution. 
| 2022-01-19 | We clarified that we need 1 feed for NL, as we can not load both Eindhoven _and_ NL including Eindhoven
| 2022-01-19 | GO Sharing notifies us that Eindhoven did not see the updated feed
| 2022-01-18 | Gemeente Eindhoven asks if feed inaccuracies are solved (no)
| 2022-01-17 | Gemeente Rotterdam asks if feed inaccuracies are solved (no)
| 2022-01-12 | Asked if there's 1 GBFS end point for all of The Netherlands. We can not read both the feed with all NL data (including Eindhoven) and the new Eindhoven feed, as it would result in duplicate data
| 2022-01-11 | GO Sharing shares 3 new GBFS URLs for Eindhoven, Rotterdam, Antwerp. It uses the latest GBFS standard and includes the vehicle types. Therefor it should fix "Uses data standard" and "Includes vehicle type"
| 2021-12-22 | Asked GO Sharing for a status update
| 2021-11-24 | GO Sharing will take action on the feed inaccuracies. Goal: static vehicle IDs, correct vehicle types, correct PROW
| 2021-11-08 | Asked GO Sharing to offer static IDs in the GBFS feed, OR offer an MDS feed. Asked GO Sharing to specify the right vehicle type (at this moment every vehicle is listed as a 'moped', even the e-bikes)
| 2021-10-14 | Activated new GBFS feed.<br /><br />goUrban updated their GBFS feed to the latest version 2.2 which resulted in the updated URLs. The main URL https://greenmo.core.gourban-mobility.com/api/gbfs is where all other supported endpoints can be found, according to the GBFS standard.<br /><br />NOTE: Vehicles now have rotating vehicle-IDs. This results in parking data being valid, but trip data is not. To meet the CROW Dashboard requirements, vehicle-IDs should be static
| 2021-10-13 | Got new GBFS feed URL via GO Sharing via goUrban
| 2021-10-11 | Asked GO Sharing to fix broken GBFS feed again (phone) -> GO Sharing is taking action
| 2021-10-07 | Asked GO Sharing to fix broken GBFS feed (phone + WhatsApp) -> GO Sharing made a ticket
| 2021-10-06 | Feed GO Sharing is broken: Authorisation key isn't valid
| 2021-09-13 | Asked GO Sharing to fix PROW and add vehicle type
