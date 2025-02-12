# Data quality: Flickbike

## Data quality status

Last updated: 2025-02-12.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ❌
| Updated <= 30s?             | ❌
| Correct PROW?               | ❌
| All NL data?                | ❌
| Includes vehicle type?      | ❌
| Offers service areas        | ❌

Status: 🔴 Unusable

## Improvements to make

### Use data standard

At the moment Flickbike is not integrated using one of the supported protocols.

Flickbike should offer the data using one of the standards: MDS or GBFS.

### Add vehicle type

🆕 The operator should communicate what kind of vehicle it's reporting. 

Since GBFS 2.1 there's a field, `vehicle_type_id`, that defines what kind of vehicle is offered.

To implement this, you can use these documentation pages: 

1. Offer [vehicle_types.json](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)
2. In free_bike_status.json, add property [vehicle_type_id](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson)

As values you can use the [latest](https://github.com/NABSA/gbfs/pull/370) standard definition for bikes:

- name: `Flickbike fiets type 1`,
- vehicle_type_id: `flickbike_type_1`
- form_factor: `bicycle`
- propulsion_type: `human`
- wheel_count: `2`

## Logs

| Updated    | Description
| ----       | ---
| 2021-09-23 | Sven asked Flickbike to offer data using a data standard
