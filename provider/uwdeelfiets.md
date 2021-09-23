# Data quality: uwdeelfiets

## Data quality status

Last updated: 2021-09-02.

| **Quality check**           | **Quality**
| --                          | -- |
| Uses data standard?         | ✅ MDS
| Updated <= 30s?             | ❔
| Correct PROW?               | ❔
| All NL data?                | ❌
| Includes vehicle type?      | ❌

Status: 🟡 Usable though needs improvement

## Improvements to make

### Offer NL data

At the moment uwdeelfiets only offers data from Haarlem. uwdeelfiets should offer data from all of NL.

### Add vehicle type & propulsion type

🆕 The operator should communicate what kind of vehicle it's reporting. 

Since GBFS 2.1 there's a field, `vehicle_type_id`, that defines what kind of vehicle is offered.

To implement this, you can use these documentation pages: 

1. Offer [vehicle_types.json](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)
2. In free_bike_status.json, add property [vehicle_type_id](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson)

As values you can use the [latest](https://github.com/NABSA/gbfs/pull/370) standard definition for bikes:

- name: `uwdeelfiets type 1`,
- vehicle_type_id: `uwdeelfiets_type_1`
- form_factor: `bicycle`
- propulsion_type: `human`
- wheel_count: `2`

To see an example, see page 2 of [this document](https://docs.google.com/document/d/1P_oDBnFvr9qzo0_5YbnrCDYptFQV9ZUOJGfi8ACD1GE/edit?usp=sharing).
