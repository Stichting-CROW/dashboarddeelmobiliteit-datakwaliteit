# Data quality: Deelfiets Nederland

## Data quality status

Last updated: 2022-05-12.

| **Quality check**           | **Quality**
| --                          | -- |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ❔
| All NL data?                | ❌
| Includes vehicle type?      | ❌
| Accuracy number of trips    | Δ = 0% 👍

Status: 🟡 Usable though needs improvement

### Explanation

- The data feed uses one of the supported standards 👍
- The feed is updated frequently 👍
- We have to check if the data specification is followed perfectly
- Deelfiets Nederland does not offers data of all vehicles ⏳
- Deelfiets Nederland does not offer 'vehicle type' in their data feed yet

The current status is 'usable though needs improvement'. As soon as all vehicle data is included, and vehicle type is added in the datafeed, the status will be 🟢 Perfect.

## Improvements to make

### Include all vehicle data

Deelfiets Nederland is active in Zwolle, Kampen, Groningen en Friesland.

At the moment only data of Zwolle en Kampen is included. The operator should include data of all their vehicles.

### Add vehicle type & propulsion type

🆕 The operator should communicate what kind of vehicle it's reporting. 

Since GBFS 2.1 there's a field, `vehicle_type_id`, that defines what kind of vehicle is offered.

To implement this, you can use these documentation pages: 

1. Offer [vehicle_types.json](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)
2. In free_bike_status.json, add property [vehicle_type_id](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson)

As values you can use the [latest](https://github.com/NABSA/gbfs/pull/370) standard definition for bikes:

- name: `Deelfiets Nederland fiets type 1`,
- vehicle_type_id: `deelfietsnederland_type_1`
- form_factor: `bicycle`
- propulsion_type: `electric_assist`
- wheel_count: `2`

To see an example, see page 2 of [this document](https://docs.google.com/document/d/1P_oDBnFvr9qzo0_5YbnrCDYptFQV9ZUOJGfi8ACD1GE/edit?usp=sharing).

## Logs

| Updated    | Description
| ----       | ---
| 2022-04-19 | We activated the new GBFS feed. Now two GBFS feeds are running simultaneously.
| 2022-04-19 | Deelfiets Nederland emails: 'We have a feed ready for you on the new platform. We can keep the old feed running on the existing URL. Simultaneously we run the new feed with most of the locations of Deelfiets Nederland. PS The new feed supports vehicle_type_id.'
| 2022-03-28 | We email: "We are happy if we can have the data of Deelfiets Nederland in the Dashboard soon. For the NS+IenW 'landelijke pilot deelfietsen op stations' this is obligated. Q: If the new feed is ready, can we keep the old feed as long as the locations of the old feed are not migrated to the new feed yet? So can we use 2 GBFS feeds until the end of 2022?"
| 2022-03-20 | Deelfiets Nederland emails: "We are migrating to a new backend. At this moment the following location use the old backend: P+R Hoogkerk Groningen, Kampen, bewaakte fietsenstalling Lubeckplein Zwolle. Most locations use the new backend, that doesn't offer a GBFS feed yet.<br /><br />We can offer a GBFS feed based on the new backend. We can support `vehicle_types` there as well. The development team expects this can be realised end of April 2022.<br /><br />In the GBFS feed based on the new backend these locations will be included: Ommen, Dalfsen, all locations in Friesland, Arnhem, Nijmegen, Enschede and most locations in Zwolle. The locations of the old feed will be gone from the moment the new feed is activated. We expect to migrate the locations from the old to new feed in the end of 2022."
| 2022-03-11 | We asked Deelfiets Nederland to include all NL vehicles in the data feed (asked before in September 2021)
| 2022-03-10 | We got an email notifying that Zwolse Deelfiets and Deelfiets Nederland are not shared, but they should. (Both brand names are part of the same company. Started as Zwolse Deelfiets, then follow up as "Deelfiets Nederland" with operations in Kampen + Friesland as well).
| 2022-03-08 | Municipality of Enschede mentions: data Deelfiets Nederland is not shared, but should be
| 2021-09-09 | Asked Deelfiets Nederland to offer all NL data and add vehicle type