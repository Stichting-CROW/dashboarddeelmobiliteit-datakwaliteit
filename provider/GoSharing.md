# Data quality: GO Sharing

## Data quality status

Last updated: 2021-09-02.

| **Quality check**            | **Quality**
| --                          | --      |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ❌
| All NL data?                | ✅
| Includes vehicle type?      | ❌
| % Accuracy number of trips  | ...

Status: 🟡 Usable though needs improvement

## Improvements to make

### Don't include mopeds that do not exist in public space

GO Sharing shares mopeds with the Dashboard Deelmobiliteit that do not exist in public space.

Properties of this type of data are that it has a GPS location in public space, the property `is_disabled` is `1` and if you walk to the bike in real life, the moped is not there.

To see examples of this type of incorrect data, [see this document](./GoSharing_extra.md).

### Add vehicle type

The operator should communicate what kind of vehicle it's reporting. 

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#vehicle-types).

For every data standard, there's documentation on how to include the vehicle type ([GBFS](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21), [MDS](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/general-information.md#vehicle-types)).

For Cykl, all vehicles are of type `bicycle`. Please include this attribute (`vehicle_type_id`) in the GBFS feed.
