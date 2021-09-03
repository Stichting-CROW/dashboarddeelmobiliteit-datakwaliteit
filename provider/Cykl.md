# Data quality: Cykl

## Data quality status

Last updated: 2021-09-02.

| **Quality check**       | **Quality**
| --                      | --          |
| Uses data standard?     | ✅ GBFS
| Updated <= 30s?         | ✅
| Correct PROW?           | ✅
| All NL data?            | ✅
| Includes vehicle type?  | ❌

Status: 🟡 Usable though needs improvement

## Improvements to make

### Add vehicle type

The operator should communicate what kind of vehicle it's reporting. 

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#vehicle-types).

For every data standard, there's documentation on how to include the vehicle type ([GBFS](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21), [MDS](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/general-information.md#vehicle-types)).

For Cykl, all vehicles are of type `bicycle`. Please include this attribute (`vehicle_type_id`) in the GBFS feed.

### Data quality statistics

Period: March 10th 2021 00:00 to March 21th 2021 00:00

| **Attribute** | **Provider** |  **Deelfietsdashboard** | **Difference in %** | 
| -- | -- |
| Number of trips | 39762
| Aantal unique id's | 39762
