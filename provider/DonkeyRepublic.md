# Data quality: Donkey Republic

## Data quality status

Last updated: 2025-10-24.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ❌
| Includes vehicle type?      | ❌

Status: 🟡 Usable though needs improvement

## Improvements to make

### Offer a MDS feed

Best is to offer a MDS feed, like in the [data spec](https://docs.dashboarddeelmobiliteit.nl/data_feeds/for_monitoring/). At the moment the GBFS feed is used (deprecated).

### Offer 1 GBFS feed for NL instead of 1 feed per city/area

It is prefered that one feed is offered for all vehicles in The Netherlands. This prevents mistakes.

### Add vehicle type

🆕 The operator should communicate what kind of vehicle it's reporting. 

Since GBFS 2.1 there's a field, `vehicle_type_id`, that defines what kind of vehicle is offered.

Please start offering vehicle type in the feed, following the GBFS standard.

To do this, you can use these documentation pages: 

1. Add [vehicle_types.json](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)
2. In free_bike_status.json, add property [vehicle_type_id](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson)

For Donkey Republic this means:

1. Add `vehicle_types.json` and include the `vehicle_types` Donkey Republic offers:
  - Bike type 1:
    - `vehicle_type_id`: `donkeyrepublic_type_x`
    - `form_factor`: `bicycle`,
    - `propulsion_type`: `human`,
    - `name`: `Donkey Republic bike type x`
  - Bike type 2:
    - `vehicle_type_id`: `donkeyrepublic_type_y`
    - `form_factor`: `bicycle`,
    - `propulsion_type`: `electric_assist`,
    - `name`: `Donkey Republic e-bike type Y`
2. In `free_bike_status.json`, add `vehicle_type_id`

To see an example, see page 2 of [this document](https://docs.google.com/document/d/1P_oDBnFvr9qzo0_5YbnrCDYptFQV9ZUOJGfi8ACD1GE/edit#).

## Logs

| Updated    | Description
| ----       | ---
| 2025-10-19 | We constateerden dat er 74 spookvoertuigen waren sinds 20 augustus 2024. Deze hebben we handmatig [verwijderd](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/issues/49#issuecomment-3419407070) van de kaart. Als je nu de data analyseert zit de foutieve data er niet meer in (74 heel lang geparkeerde voertuigen). Als je echter tussen 20 augustus 2024 en 19 oktober 2025 analyses hebt gedaan op stilstandsduur, dan wordt deze mogelijk beinvloed door de onjuiste parkeerduur van 74 voertuigen. Bij vragen hierover: contact info@dashboarddeelmobiliteit.nl
| 2024-10-07 | Donkey Republic biedt nu ook data in Zwijndrecht, Papendrecht en Sliedrecht
| 2024-07-04 | Donkey Republic biedt nu ook data in Leiden, Katwijk en Oegstgeest
