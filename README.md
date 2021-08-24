# Dashboard Deelmobiliteit data quality

Below we document the data quality of the feeds offered by the providers.

## Data quality status

| **Provider** | **Status** ¹ | Uses standard ² | Updated <= 30s ³ | Correct PROW <sup>4</sup> | NL data <sup>5</sup> | Vehicle type <sup>6</sup> |
| :----------- | :--------: | :------------ | :------------: | :----------: | :-----: | :----------: |
| Cykl     |  🟡        | ✅ GBFS        | ✅             | ✅           | ✅      | ❌
| Flickbike | 🔴         | ❌           | ❌             | ❌          | ❌       | ❌
| Donkey Republic | 🟡     | ✅ GBFS      | ✅             | ❌           | ✅       | ❌
| Mobike     | 🔴          | ❌          | ❌              | ➖          | ❌      | ❌
| HTM        | 🔴          | ✅ GBFS      | ❌             | ❔          | ❌        | ❌
| GO Sharing | 🟡           | ✅ GBFS     | ✅             | ❌          | ✅       | ❌
| CHECK      | 🟡             | ✅ GBFS     | ✅            | ❔         | ✅       | ❌
| Felyx      | 🟡            | ✅ GBFS      | ❌ 300s         | ❌         | ❌       | ❌
| Deelfiets Nederland | 🟡    | ✅ GBFS     | ✅           | ❔         | ❌       | ❌
| Keobike    | 🟡            | ✅ GBFS     | ✅           | ❔         | ✅       | ❌
| Lime       | 🔴          | ❌ GBFS<br>rotated IDs | ✅       | ❔          | ✅      | ❌
| BAQME      | 🟡          | ✅ GBFS        | ✅           | ❔         | ❌       | ❌
| Cargoroo   | 🟡          | ✅ GBFS        | ✅           | ❔         | ✅       | ❌
| uwdeelfiets | 🔴          | ✅ MDS        | ❔           | ❔         | ❌       | ❌

🟢 = Perfect
🟡 = Usable though needs improvement
🔴 = Unusable

### ℹ️ Status <sup>1</sup>

There are three statusses:
- 🟢 Perfect
- 🟡 Usable though needs improvement
- 🔴 Unusable

### ℹ️ Uses standard <sup>2</sup>

As documented in the [dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/), data has to be shared using one of the following data standards:

- MDS
- GBFS
- TOMP

There is one additional requirements:

- All vehicles must have a static ID

### ℹ️ Updated <= 30s <sup>3</sup>

As [documented](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#general) in the dataspec, the data feed must be updated at least every 30 seconds.

### ℹ️ Correct PROW <sup>4</sup>

We use the PROW as described in the [MDS standard](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/provider/README.md#mobility-data-specification-provider) for determining if a vehicle should be included in the datafeed or not. Also the MDS standard defines what [vehicle status](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/general-information.md#state-machine-diagram) should be shared.

A vehicle should only be included if:

- The vehicle is in public space, available and not rented out
- The vehicle is in public space and reserved
- The vehicle is in public space and disabled
- The vehicle is in public space and defect

If a vehicle is reserved, disabled or defect, the vehicle status must be included as described in the data standard.

NOTE: If a vehicle is not present in public space (because it's stolen), the vehicle should be excluded from the data feed.

### ℹ️ NL data <sup>5</sup>

The operator should provide data of all their vehicles in The Netherlands.

### ℹ️ Vehicle type <sup>6</sup>

(new) The operator should communicate what kind of vehicle it's reporting. 

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#vehicle-types).

For every data standard, there's documentation on how to include the vehicle type ([GBFS](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21), [MDS](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/general-information.md#vehicle-types)).
