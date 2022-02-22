# Data quality: HTM

## Data quality status

Last updated: 2022-02-22.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ❌ GBFS
| Updated <= 30s?             | ➖
| Correct PROW?               | ➖
| All NL data?                | ➖
| Includes vehicle type?      | ➖

Status: 🔴 Unusable

## Improvements to make

### Use data standard

At the moment HTM offers a GBFS feed having incorrect data.

HTM should offer the data using one of the standards: MDS, GBFS or TOMP. Preferably MDS.

### Add vehicle type

🆕 The operator should communicate what kind of vehicle it's reporting. 

Since GBFS 2.1 there's a field, `vehicle_type_id`, that defines what kind of vehicle is offered.

To implement this, you can use these documentation pages: 

1. Offer [vehicle_types.json](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)
2. In free_bike_status.json, add property [vehicle_type_id](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson)

As values you can use the [latest](https://github.com/NABSA/gbfs/pull/370) standard definition for mopeds:

- name: `HTM fiets type 1`,
- vehicle_type_id: `htm_type_1`
- form_factor: `moped`
- propulsion_type: `electric`
- wheel_count: `2`

To see an example, see page 2 of [this document](https://docs.google.com/document/d/1P_oDBnFvr9qzo0_5YbnrCDYptFQV9ZUOJGfi8ACD1GE/edit?usp=sharing).


## Logs

| Updated    | Description
| ----       | ---
| 2022-02-22 | We email Joyride: Do you have a MDS feed available for us?
| 2022-01-25 | HTM sends a feed URL that has 'mds' in the URL path but isn't MDS
| 2022-01-24 | We email HTM: Could you ask your development partner if a MDS feed can be shared?
| 2022-01-19 | We email HTM: 'The data is in the Dashboard, but is not of high quality. We expect dynamic IDs are used instead of static IDs. The best option would be to offer a MDS data feed'.
| 2022-01-19 | HTM emails: any updates?
| 2021-12-22 | The HTM data that was shared by spreadsheet is not equal to the HTM data shared by the GBFS feed. We disable the feed, share our findings with HTM and ask to improve/fix the GBFS feed
| 2021-12-10 | HTM sent the amount of trips for November 24th to December 10th. We will do a comparison
| 2021-12-10 | We tested the feed. There're static IDs now, which is good. We see that there're less trips than park events though. We asked HTM for the amount of HTM trips for November 24th to December 10th
| 2021-10-26 | HTM sent a new GBFS URL. We will test this
