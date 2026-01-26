# Dashboard Deelmobiliteit data quality

Below we document the data quality of the feeds offered by the providers.

## Data quality status

| **Provider**                                                                                                                                                                     | **Status** ¹ | Uses standard ² | Updated <= 30s ³ | Correct PROW <sup>4</sup> | Vehicle type <sup>6</sup> | Service areas <sup>7</sup> |
| :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------: | :-------------- | :--------------: | :-----------------------: | :-----------------------: | :------------------------: |
| [BAQME](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/BAQME.md)                                                                     |      🟢      | ✅ MDS          |        ✅        |            ✅             |            ✅             |             ❌             |
| [CHECK](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/CHECK.md)                                                                     |      🟡      | ✅ MDS          |        ✅        |            ✅             |            ✅             |             ✅             |
| [Cargoroo by MOBYU](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Cargoroo.md)                                                      |      🟡      | ✅ MDS          |        ✅        |            ✅             |            ❌             |             ❌             |
| [Cykl](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Cykl.md)                                                                       |      🟡      | ✅ GBFS         |        ✅        |            ✅             |            ❌             |             ❌             |
| [Deelfiets Nederland](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/DeelfietsNederland.md)                                          |      🟢      | ✅ GBFS         |        ✅        |            ✅             |            ✅             |             ❌             |
| [Donkey Republic](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/DonkeyRepublic.md)                                                  |      🟡      | ✅ GBFS         |        ✅        |            ✅             |            ❌             |             ❌             |
| [Dott](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Dott.md)                                                                       |      🟢      | ✅ MDS          |        ✅        |            ✅             |            ✅             |             ❌             |
| [Felyx](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Felyx.md)                                                                     |      🟢      | ✅ MDS 1.2, GBFS 3.0          |        ✅        |            ✅             |            ✅             |             ✅             |
| [GO Sharing](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/GoSharing.md)                                                            |      🟡      | ✅ MDS          |        ❌        |            ✅             |            ✅             |             ❌             |
| [Greenwheels](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Greenwheels.md)                                                         |      🔴      | ❌ MDS          |        ➖        |            ➖             |            ➖             |
| [HTM](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/HTM.md)                                                                         |      🔴      | ❌ MDS          |        ➖        |            ➖             |            ➖             |             ❌             |
| [Lime](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Lime.md)                                                                       |      🟢      | ✅ MDS          |        ✅        |            ✅             |            ✅             |             ❌             |
| [MoveYou](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/MoveYou.md)<br /><sub><sup>- GoAbout<br />- Deelfietsen Zeeland</sub></sup> |      🟡      | ✅              |        ✅        |            ✅             |            ❌             |             ❌             |
| [MyWheels](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/MyWheels.md)                                                               |      🔴      | ❌ MDS          |        ➖        |            ➖             |            ➖             |             ➖             |
| OV-fiets                                                                                                                                                                         |      🔴      | ❌              |        ➖        |            ➖             |            ➖             |             ➖             |
| [TIER](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/TIER.md)                                                                       |      ⚪      | ✅ MDS          |        ❌        |            ❔             |            ❌             |             ❌             |
| Deelbuggy's / Wilmar                                                                                                                                                             |      ➖      | ➖              |        ➖        |            ➖             |            ➖             |             ➖             |

🟢 = Perfect
🟡 = Usable though needs improvement
🔴 = Unusable
⏳ = Integration in process

### ℹ️ Status <sup>1</sup>

There are four statuses:

- 🟢 Perfect
- 🟡 Usable though needs improvement
- 🔴 Unusable
- ⏳ Integration in process

### ℹ️ Uses standard <sup>2</sup>

As documented in the [dataspec](https://docs.dashboarddeelmobiliteit.nl), data has to be shared using one of the following data standards:

- MDS
- GBFS
- TOMP

MDS is the prefered data standard to use for offering vehicle and rental data, as well as exchanging zone policies.

GBFS is used for sharing service areas and geofencing zones.

### ℹ️ Updated <= 30s <sup>3</sup>

As [documented](https://docs.dashboarddeelmobiliteit.nl/data_feeds/for_monitoring/#data-specifications) in the dataspec, the data feed must be updated at least every 30 seconds.

### ℹ️ Correct PROW <sup>4</sup>

We use the PROW as described in the [MDS standard](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/provider/README.md#mobility-data-specification-provider) for determining if a vehicle should be included in the data feed or not. Also the MDS standard defines what [vehicle status](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/general-information.md#state-machine-diagram) should be shared.

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

The operator should communicate what kind of vehicle it's reporting.

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.dashboarddeelmobiliteit.nl/data_feeds/for_monitoring/#how-to-offer-vehicle-type-in-mds).

For every data standard, there's documentation on how to include the vehicle type ([GBFS](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21), [MDS](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/general-information.md#vehicle-types)).

### ℹ️ Service areas <sup>7</sup>

The operator could share its service areas using a GBFS feed as [explained here](https://docs.dashboarddeelmobiliteit.nl/data_feeds/service_areas/). If the operator shares its service areas, these can be shown in the Dashboard Deelmobiliteit at [dashboarddeelmobiliteit.nl/map/servicegebieden](https://dashboarddeelmobiliteit.nl/map/servicegebieden). Historical changes are then stored automatically as well, so you can easily see the development through time.

## Integrations by external parties

The public data feed of CROW Dashboard Deelmobiliteit is currently used by the following tools:

- Rotterdam PowerBI Mobiliteit Dashboard (2024-2025)
- [Zwolle arcgis data portal](https://www.arcgis.com/home/item.html?id=ec6f32f71d1f413ebbcbc3bc6a0e1151) (2023-2025)

## Logos of providers connected to Dashboard Deelmobiliteit

<img alt="Cykl" src="https://www.cykl.nl/img/cykl_word.png" width="100" />

<img alt="Donkey Republic" src="https://cdn.donkey.bike/wp-content/uploads/2016/04/16121255/New-logo-small.png" width="100" />

<img alt="HTM" src="https://www.htm.nl/media/ukygkkaq/htm-logo_def.svg" width="100" />

<img alt="GO Sharing" src="https://nl.go-sharing.com/app/uploads/2021/01/logo@2x.png" width="100" />

<img alt="CHECK" src="https://images.prismic.io/ridecheck/2e5103fa-6f51-4e52-844c-f35b14ae63ae_Check_Wordmark_Black.png?auto=compress,format" width="100" />

<img alt="Felyx" src="https://images.crunchbase.com/image/upload/c_pad,h_170,w_170,f_auto,b_white,q_auto:eco,dpr_2/iignk4msnfnxzombin4g" width="100" />

<img alt="Deelfiets Nederland" src="https://www.deelfietsnederland.nl/wp-content/uploads/2019/11/HL2mPwHA-300x236.png" width="100" />

<img alt="Lime" src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/04/Lime_Logos-wiki-01.svg/2560px-Lime_Logos-wiki-01.svg.png" width="100" />

<img alt="BAQME" src="https://www.baqme.com/wp-content/uploads/2021/01/BAQME_Logo_Black@3x-1.png" width="100" />

<img alt="Cargoroo" src="https://cargoroo.nl/wp-content/uploads/2021/11/Cargoroo-web-logo-1.png" width="100" />

<img alt="Uw Deelfiets" src="https://www.uwdeelfiets.nl/wp-content/uploads/2021/06/uw-deelfiets-2021-logo-2.svg" width="100" />

<img alt="Bird" src="https://mms.businesswire.com/media/20220125005267/en/1308263/5/Bird_Logo_Lockup_ko.jpg" width="100" />

<img alt="Bolt" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/17/Bolt_logo.png/1200px-Bolt_logo.png?20190831113556" width="100" />

<img alt="Bondi" src="https://bondi.city/assets/img/bondi_logo_blue.jpeg" width="100" />

Providers above were actively sharing data on 2022-09-14.
