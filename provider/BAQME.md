# Data quality: BAQME

## Data quality status

Last check: 2023-07-07.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ MDS
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ✅

Status: 🟡 Usable though needs improvement

## Improvements to make

### Bied 1 MDS-feed aan voor heel Nederland

Momenteel worden 4 MDS-feeds aangeleverd, voor elke vloot 1. Liever ontvangen we 1 MDS-feed met alle NL voertuigen.

## Logs

| Updated    | Description
| ----       | ---
| 2023-08-01 | 🐛 -> ✅ In het Ontwikkeling-scherm van het Dashboard Deelmobiliteit is het aantal beschikbare voertuigen te hoog in de periode 7 juli en 1 augustus 2023. De oorzaak was dat BAQME sinds de nieuwe MDS-feed gebruikt maakt van ander type voertuig-IDs, bijvoorbeeld `baqme:bq0251` ipv `baqme:7a007b55-1b50-4ec6-a1f0-85a8245242be`. We hebben alle parkeerperiode's van de voertuigen met oude voertuig-IDs handmatig beeindigd, met als ingesteld eindtijd: end_time = start_time. Uitgevoerde query: `UPDATE park_events SET end_time = start_time WHERE system_id = 'baqme' AND end_time IS NULL AND start_time <= '2023-07-08';` resulteerde in 265 updates.
| 2023-07-12 | ✅ BAQME heeft de waardes voor voertuigtypes en aandrijving gewijzigd in 'elektrisch' en 'bakfiets' - dit staat nu goed.
| 2023-07-07 | 🐛 De voertuigen die BAQME aanlevert staan vermeld als 'fiets' en 'mensaangedreven'. Het zijn echter elektrische bakfietsen. We vragen dit te updaten.
| 2023-07-07 | ✅ De 4 nieuwe MDS-feeds zijn geactiveerd en de GBFS-feed is gedeactiveerd. De feeds zouden nu weer moeten resulteren in juiste verhuurdata
| 2023-06-29 | 🐛 Wij ontvangen links naar de MDS-feeds van BAQME 👍
| 2023-06-22 | 🐛 BAQME geeft aan dat er al een MDS-feed is voor Rotterdam. BAQME kan een samengestelde MDS-feed aanleveren met data van alle fleets. Wordt vervolgd.
| 2023-06-13 | 🐛 Gemeente Den Haag merkt op dat er geen verhuringen van BAQME te zien zijn, terwijl die er wel verhuringen moeten zijn. Wij zien dat de GBFS-feed van BAQME sinds enige tijd roterende ID's heeft, hetgeen niet werkt in combinatie met het Dashboard Deelmobiliteit. Wij noemen dat MDS of GBFS 1.0 ondersteund worden. Zo te zien geeft de GBFS feed met roterende ID's problemen sinds 3 april 2023.
| 2023-03-07 | ✅ The data outage is fixed at 17:32 today. There're new, seperate GBFS feeds instead of 1 combined feed: https://baqmefleet.com/generate_full_feed.php?fleet=rtm and https://baqmefleet.com/generate_full_feed.php?fleet=dh. We prefer 1 combined feed. BAQME sais it will offer the data in 1 combined feed again.
| 2023-03-03 | 🐛 There's a data outage. We didn't receive data from the GBFS end point anymore since yesterday 8am and today. Reason was an app migration at/to Joyride.
| 2022-08-15 | BAQME emails us: 'At the moment Joyride doesn't give priority to updating the feed so it follows the GBFS standard (`is_reserved` property). We/BAQME updated our "old" custom made BAQME feed. It should give accurate data now.'
| 2022-08-15 | We didn't get any response from Joyride.
| 2022-07-19 | The Joyride GBFS feed has no rotated ID's, but it doesn't remove vehicles from the feed if these are in active rental ([though they should](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_statusjson)). We emailed Joyride and ask if they can fix the GBFS feed so it doesn't include vehicles that have an active rental.
| 2022-07-09 | We added the new GBFS feed for testing purposes.
| 2022-06-28 | BAQME asks us if we can activate the GBFS feed of joyridecity.bike, so that BAQME's can disable its own feed and save resources. 
| 2022-03-21 | BAQME emails: "We got a GBFS feed URL from our whitelabel software provider. Could you check if this feed is valid and that is does have static vehicle IDs?"
| 2022-01-31 | There has been 'fake' vehicle at [51.9103119, 4.4782139] from 2021-09-06 to 2022-01-26 11:00. Reason was: Joyride often sends this exact coordinate if there's a status change. BAQME fixed this in their feed and asked Joyride to fix it at there side as well. Since 2022-01-26 this 'fake' vehicle is not present in the data feed anymore, so all is good now
| 2021-09-09 | Asked BAQME to add vehicle type
