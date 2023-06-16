# Data quality: Donkey Republic

## Data quality status

Last checked at 2023-06-15.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ❌
| All NL data?                | ✅
| Includes vehicle type?      | ❌

Status: 🟡 Usable though needs improvement

## Improvements to make

### Share bicycles that are parked outside hubs

We do not get all unrented vehicles that are parked in public space. We get the parked vehicles inside hubs, but we don't get parked vehicles outside hubs. Please offer all vehicles that are parked in public space, in your data feed.

### Offer a MDS feed

Best is to offer a MDS feed, like in the [data spec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#general). At the moment the GBFS feed is used (deprecated).

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
| 2023-06-16 | We vragen Donkey Republic per mail om het datafeed-probleem op te lossen (geef alle geparkeerde voertuigen terug, ook voertuigen buiten hubs)
| 2023-05-23 | Gemeente Amsterdam merkt op dat 'misplaced' voertuigen (voertuigen geparkeerd buiten Donkey-hubs) niet in het Dashboard staan. We hadden hier in februari al contact over opgenomen met Donkey Republic, maar hier is nog niets mee gedaan
| 2023-03-13 | We hebben de GBFS-feed van Donkey/Gorinchem toegevoegd; er is vanaf vandaag data van Gorinchem in het Dashboard Deelmobilitit
| 2023-03-13 | Donkey deelt het `city ID` van Gorinchem (515)
| 2023-03-08 | We vragen Donkey Republic om het `city ID` van Gorinchem te delen
| 2023-03-07 | Donkey deelt de reden dat Gorinchem mist in de data: Drechtsteden en Rotterdam zijn gesplitst in het systeem van Donkey (voorheen vielen ze onder 1 account en dus 1 GBFS-feed)
| 2023-02-13 | Provincie Zuid-Holland meldt dat Gorinchem mist in het Dashboard. Fietsen rijden al - officiële opening is 9 maart
| 2023-02-13 | Gemeente Rotterdam emails: 40 New Donkey Republic bikes that are in public space are not in the GBFS-feed
| 2022-06-14 | We confirmed: The GBFS feeds are working well again.
| 2022-06-13 | Donkey Republic emails: "If I'm right the feed data should now be available again"
| 2022-06-07 | We email and ask for an update.
| 2022-05-28 | We email and ask for an update.
| 2022-05-19 | Donkey emails: 'I send this to our backend/data team. Hopefully there's an solution soon'
| 2022-05-18 | We email Donkey en mention: 'Since April 23th the GBFS feeds are not updated anymore. Can you look into this?'
| 2022-01-21 | Added Donkey data to the Dashboard, by adding the Dordrecht feed manually. See point of improvement #3 to prevent this in the future
| 2022-01-21 | Dordrecht data is not included in the feed at the moment
| 2021-11-08 | Asked Donkey Republic to fix PROW (especially 1.2)
| 2021-09-10 | Donkey Republic forwarded info to J responsible for its software development
| 2021-09-09 | Asked Donkey Republic to fix PROW and add vehicle type
