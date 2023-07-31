# Dashboard Deelmobiliteit data quality

Below we document the data quality of the feeds offered by the providers.

## Data quality status

| **Provider**                                                                                                                  | **Status** ¹ | Uses standard ² | Updated <= 30s ³ | Correct PROW <sup>4</sup> | NL data <sup>5</sup> | Vehicle type <sup>6</sup> |
| :-----------                                                                                                                  | :--------:   | :------------   | :------------:   | :----------:       | :-----:                     | :----------:              |
| Arriva Schinnen                                                                                                               | ⏳           | ➖              | ➖                | ➖                 | ➖                         | ➖
| Arriva/Bravo/Hopperpoint                                                                                                      | 🔴           | ❌              | ➖                | ➖                 | ➖                         | ➖
| [BAQME](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/BAQME.md)                  | 🟢           | :heavy_check_mark: MDS         | :heavy_check_mark:                | :heavy_check_mark:                 | :heavy_check_mark:                         | :heavy_check_mark:
| [Bird](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Bird.md)                    | 🟢           | :heavy_check_mark: MDS             | :heavy_check_mark:               | :heavy_check_mark:                  | :heavy_check_mark:                         | :heavy_check_mark:
| [Bolt](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Bolt.md)                    | 🟢           | :heavy_check_mark: MDS           | :heavy_check_mark:                | :heavy_check_mark:                 | :heavy_check_mark:                         | :heavy_check_mark:
| [Bondi](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Bondi.md)                  | 🟡           | :heavy_check_mark: GBFS           | :heavy_check_mark:                | ❔                 | :heavy_check_mark:                         | ❌
| [Cargoroo](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Cargoroo.md)            | 🟡           | :heavy_check_mark: GBFS | :heavy_check_mark: | ❔                 | :heavy_check_mark:                         | ❌
| Century      | 🔴           | ❌             | ❌              | ❌                           | ❌                 | ❌
| [CHECK](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/CHECK.md)                  | 🔴           | :heavy_check_mark: GBFS | :heavy_check_mark: | ❌ | :heavy_check_mark:                         | ❌
| [Cykl](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Cykl.md)                    | 🟡           | :heavy_check_mark: GBFS | :heavy_check_mark: | :heavy_check_mark:                 | :heavy_check_mark:                         | ❌
| [Deelfiets Nederland](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/DeelfietsNederland.md) | 🟡 | :heavy_check_mark: GBFS | :heavy_check_mark: | :heavy_check_mark:                 | :heavy_check_mark:                         | ❌
| [Donkey Republic](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/DonkeyRepublic.md) | 🟡         | :heavy_check_mark: GBFS | :heavy_check_mark: | ❌                 | :heavy_check_mark:      | ❌
| [Felyx](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Felyx.md)                  | 🟡           | :heavy_check_mark: GBFS         | ❌<br><sub><sup>300s</sup></sub> | ❌  | :heavy_check_mark:                         | ❌
| [Flickbike](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Flickbike.md)          | 🔴           | ❌              | ➖                | ➖                 | ➖                         | ➖
| [GO Sharing](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/GoSharing.md)         | 🟡           | :heavy_check_mark: MDS       | :heavy_check_mark:                | ❌          | :heavy_check_mark:                         | :heavy_check_mark:
| [Greenwheels](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Greenwheels.md)      | 🔴           | ❌ MDS             | ❌              | ❌                           | ❌                 | ❌
| GAON      | 🔴           | ❌             | ❌              | ❌                           | ❌                 | ❌
| Hely                                                                                                                          | 🟡           | :heavy_check_mark: TOMP         | ❔                | ❔                 | ❔                         | ❔
| [HTM](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/HTM.md)                      | 🔴           | ❌ MDS         | ➖                | ➖                 | ➖                         | ➖
| [Keobike](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Keobike.md)              | 🟡           | :heavy_check_mark: GBFS         | :heavy_check_mark:                | ❔                 | :heavy_check_mark:                          | ❌
| [Lime](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Lime.md)                    | 🟢           | MDS | :heavy_check_mark: | :heavy_check_mark:   | :heavy_check_mark:                         | :heavy_check_mark:
| [Movelo](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Movelo.md)                | ➖           | ➖              | ➖                | ➖                 | ➖                         | ➖
| [MoveYou](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/MoveYou.md)<br /><sub><sup>- GoAbout<br />- Deelfietsen Zeeland</sub></sup> | 🟡 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark:    | :heavy_check_mark:                         | ❌
| nextbike                                                                                                                      | 🔴           | ❌              | ➖                | ➖                 | ➖                         | ➖
| OV-fiets                                                                                                                      | 🔴           | ❌              | ➖                | ➖                 | ➖                         | ➖
| [Promo-Bikey](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/Promo-Bikey.md)      | ➖           | ➖              | ➖                | ➖                 | ➖                         | ➖
| [SHARE NOW](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/SHARENOW.md)           | 🔴           | ❌              | ➖                | ➖                 | ➖                         | ➖
| [TIER](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/TIER.md)                    | 🟢           | :heavy_check_mark: MDS              | :heavy_check_mark: | ❔                         | :heavy_check_mark:                         | :heavy_check_mark:
| Urbee                                                                                                                         | ⏳           | ➖              | ➖                | ➖                 | ➖                         | ➖
| [uwdeelfiets](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/blob/main/provider/uwdeelfiets.md)      | 🟡           | :heavy_check_mark: MDS | ❔         | ❔                 | ❌                         | ❌
| Vaimoo/GoBike                                                                                                                 | 🔴           | ❌              | ➖                | ➖                 | ➖                         | ➖
| Velocity Limburg                                                                                                              | ➖           | ➖              | ➖                | ➖                 | ➖                         | ➖
| Deelbuggy's / Wilmar                                                                                                           | ➖           | ➖              | ➖                | ➖                 | ➖                         | ➖
| X-bike                                                                                                                        | ⏳           | ➖              | ➖                | ➖                 | ➖                         | ➖

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

As documented in the [dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/), data has to be shared using one of the following data standards:

- MDS
- GBFS
- TOMP

There is one additional requirement:

- All vehicles must have a static ID

MDS is the prefered data standard to use.

### ℹ️ Updated <= 30s <sup>3</sup>

As [documented](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#general) in the dataspec, the data feed must be updated at least every 30 seconds.

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

To decide on what vehicle type should be reported, use the [table in our dataspec](https://docs.crow.nl/deelfietsdashboard/hr-dataspec/#vehicle-types).

For every data standard, there's documentation on how to include the vehicle type ([GBFS](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21), [MDS](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/general-information.md#vehicle-types)).

## Integrations by external parties

The public data feed of CROW Dashboard Deelmobiliteit is currently used by the following tools:

- [Zwolle arcgis data portal](https://www.arcgis.com/home/item.html?id=ec6f32f71d1f413ebbcbc3bc6a0e1151)

## Logos of providers connected to Dashboard Deelmobiliteit

<img alt="Cykl" src="https://www.cykl.nl/img/cykl_word.png" width="100" />

<img alt="Donkey Republic" src="https://cdn.donkey.bike/wp-content/uploads/2016/04/16121255/New-logo-small.png" width="100" />

<img alt="HTM" src="https://www.htm.nl/typo3conf/ext/htm_template/Resources/Public/img/logo.svg" width="100" />

<img alt="GO Sharing" src="https://nl.go-sharing.com/app/uploads/2020/11/logo@2x.png" width="100" />

<img alt="CHECK" src="https://cdn.homerun.co/53887/check-wordmark-black4x-31571056630logo.png" width="100" />

<img alt="Felyx" src="https://cdn.felyx.com/uploads/2021/03/010720-Felyx-logo.png" width="100" />

<img alt="Deelfiets Nederland" src="https://www.deelfietsnederland.nl/wp-content/uploads/2019/11/HL2mPwHA-300x236.png" width="100" />

<img alt="KeoBike" src="https://www.keobike.nl/App_Themes/Syntus/img/logo-keobike.png" width="100" />

<img alt="Lime" src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/04/Lime_Logos-wiki-01.svg/2560px-Lime_Logos-wiki-01.svg.png" width="100" />

<img alt="BAQME" src="https://www.baqme.com/wp-content/uploads/2021/01/BAQME_Logo_Black@3x-1.png" width="100" />

<img alt="Cargoroo" src="https://cargoroo.nl/wp-content/uploads/2021/11/Cargoroo-web-logo-1.png" width="100" />

<img alt="Uw Deelfiets" src="https://www.uwdeelfiets.nl/wp-content/uploads/2021/06/uw-deelfiets-2021-logo-2.svg" width="100" />

<img alt="hely" src="https://hely.com/static/images/hely-logo.svg" width="100" />

<img alt="TIER" src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/32/TIER_Mobility_Logo_%28blau%2C_2021%29.svg/512px-TIER_Mobility_Logo_%28blau%2C_2021%29.svg.png" width="100" />

<img alt="Bird" src="https://mms.businesswire.com/media/20220125005267/en/1308263/5/Bird_Logo_Lockup_ko.jpg" width="100" />

<img alt="Bolt" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/17/Bolt_logo.png/1200px-Bolt_logo.png?20190831113556" width="100" />

<img alt="Bondi" src="https://upload.wikimedia.org/wikipedia/commons/d/dd/Bondi.city_logo.png" width="100" />

<img alt="moveyou" src="https://moveyou.com/wp-content/themes/moveyou/assets/gfx/brand-large.svg" width="100" />

Providers above were actively sharing data on 2022-09-14.
