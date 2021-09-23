# Data quality: Deelfiets Nederland

## Data quality status

Last updated: 2021-09-09.

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
| 2021-09-09 | Asked Deelfiets Nederland to offer all NL data and add vehicle type