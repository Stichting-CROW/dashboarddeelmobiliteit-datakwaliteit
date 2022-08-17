# Data quality: Provider name

## Data quality status

Last updated at 2022-09-02.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ❌
| Correct PROW?               | ❌
| All NL data?                | ❌
| Includes vehicle type?      | ❌
| % Accuracy number of trips  | ...

Status: 🔴 Unusable
Status: 🟡 Usable though needs improvement
Status: 🟢 Perfect

## Improvements to make

### Add vehicle type

The operator should communicate what kind of vehicle it's reporting. 

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#vehicle-types).

For every data standard, there's documentation on how to include the vehicle type ([GBFS](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21), [MDS](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/general-information.md#vehicle-types)).

For Cykl, all vehicles are of type `bicycle`. Please include this attribute (`vehicle_type_id`) in the GBFS feed.

## Logs

| Updated    | Description
| ----       | ---
| 2021-09-23 | A log description
