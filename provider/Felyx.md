# Data quality: Felyx

## Data quality status

Last updated: 2025-05-20

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ MDS 1.2, GBFS 3.0
| Updated <= 30s?             | ✅
| Correct [PROW](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit#%E2%84%B9%EF%B8%8F-correct-prow-4)?               | ❌
| All NL data?                | ✅
| Includes vehicle type?      | ✅
| Offers service areas        | ✅ maar alleen van scooters/brommers, niet van e-fietsen

Status: 🔴 Unusable

## Improvements to make

- Offer service areas of e-bikes using a GBFS geofencing_zones feed

## Logs

| Updated    | Description
| ----       | ---
| 2026-05-19 | 🐛 Felyx en DD dev team hebben een online meeting. DD heeft een export gestuurd van alle ritten die nog openstaan, verzocht dat Felyx snel een paar checks doet en dan Cooltra verzoekt bugs op te lossen in de datafeed als dingen niet kloppen
| 2026-05-18 | 🐛 Ook Nijmegen meldt dat in het DD voertuigen staan die niet in de Felyx-app staan
| 2026-04-22 | 🐛 Gemeente Rotterdam ziet verschillen in data van Felyx in DD en data gekregen van Felyx. Dashboard Deelmobiliteit heeft het onderzocht en ziet geen grote fouten in de verwerking van data; het lijkt aan datakwaliteit van de datafeed te liggen. Het probleem lijkt dat voertuigen naar het depot worden gebracht, maar niet worden afgemeld in de de data die het Dashboard Deelmobiliteit ontvangt (de voertuigen blijven in de datafeed aangeleverd worden)
| 2025-11-28 | 🐛 Gemeente Nijmegen constateert dat servicegebieden van e-bikes niet worden aangeleverd in de servicegebieden-feed. We vragen na of de servicegebieden van e-bikes ook in een GBFS-feed aangeleverd kunnen worden
| 2025-07-08 | 🎉 Felyx levert nu ook **servicegebieden van alle NL steden** via hun GBFS-feed
| 2024-11-05 | De datakwaliteit voor Felyx is op orde: er is maximaal 1% verschil in verhuringencijfers. Felyx heeft verhuringendata gestuurd voor 29 en 30 oktober (Rotterdam en heel NL). Die we hebben vergeleken.<br />- October 29th - Rotterdam: Dashboard vs Felyx data +1%<br />- October 30th - Rotterdam: Dashboard vs Felyx data +1% <br />- October 29th - Nederland: Dashboard vs Felyx data -1% <br />- October 30th - Nederland: Dashboard vs Felyx data +1%
| 2024-10-31 | We hebben Felyx cijfers van het Dashboard gestuurd (aanbod/verhuringen), met de vraag deze vergelijken met de cijfers bekend bij Felyx. Zo weten we straks of de data in het Dashboard Deelmobiliteit gelijk is aan de cijfers bij Felyx.
| 2024-10-12 | 🎉 **VERHURINGEN KLOPPEN WEER BEHOORLIJK** - De verhuringen-cijfers kloppen sinds de update van gisteren veel beter, met 7-14% afwijking in aantal verhuringen. Er moet nog een datafeed-foutoplossing gedaan worden door Cooltra: "There is an incorrect 'removed' state when a vehicle is marked for recollection. We are talking with Operations about this topic"
We are still talking with Operations about this topic. I will keep you posted.
| 2024-10-11 | Het ontwikkelteam van Cooltra heeft de datafeed geupdate. "We stopped showing a non_operational state while the vehicle was with a customer." Wij testen de datafeed.
| 2024-10-09 | Er zijn meerdere problemen met de last_vehicle_state, o.a. non_operational state i.p.v. on_trip state gedurende een rit en removed state voor voertuigen die niet beschikbaar zijn maar nog wel in de openbare ruimte staan terwijl non_operational de juiste staat is. Over deze problemen is contact en Felyx is actief bezig deze op te lossen.
| 2024-09-21 | De datafeed van Felyx wordt nu aangeboden door software van Cooltra. Sinds vandaag deelt Felyx een nieuwe MDS-feed met de voertuigen. We hebben de oude GBFS-feed gedeactiveerd en de nieuwe MDS-feed rond 14:00 uur geactiveerd.
| 2024-09-09 | Gemeente Den Haag meldt dat het aantal verhuringen sinds 21 augustus ineens een stuk lager is dan eerder. Felyx geeft aan dat er sinds de overgang inderdaad iets mis is in hun nieuwe datafeed, waardoor het aantal trips niet klopt. Felyx werkt aan een oplossing.
| 2024-08-21 | 🐛 **VERHURINGEN KLOPPEN NIET** - Per vandaag wordt de MDS-feed gebruikt in plaats van de oude GBFS-feed
| 2024-07-04 | Felyx is gestart met aanbieden van voertuigen in Hilversum
| 2024-07-04 | We hebben de voertuigdata van Felyx vergeleken met die van het Dashboard Deelmobiliteit, voor 29 juni t/m 1 juli. Elke dag kwam het aantal voertuigen in het Dashboard Deelmobiliteit en in het Felyx dashboard precies overeen, specifiek voor gemeente Zwolle. De datakwaliteit is hier dus perfect op orde.