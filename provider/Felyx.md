# Data quality: Felyx

## Data quality status

Last checked at 2025-02-12.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ MDS 1.2
| Updated <= 30s?             | ✅
| Correct [PROW](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit#%E2%84%B9%EF%B8%8F-correct-prow-4)?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ✅
| Offers service areas        | ❌

Status: 🟢 Usable though needs improvement

## Improvements to make

- Offer service areas using a GBFS geofencing_zones feed

## Logs

| Updated    | Description
| ----       | ---
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
| 2022-10-18 | Municipality of The Hague emails Felyx and asks: Can you update the feed so it shared data every 30 seconds instead of 5 minutes? The Hague needs this for the micro hubs functionality
| 2022-09-12 | Felyx does share Tilburg data with Dashboard Deelmobiliteit again. We are missing Tilburg Felyx data from September 8th until 12th
| 2022-09-08 | Felyx doesn't share Tilburg data anymore. We contacted Felyx
| 2022-05-19 | Gemeente Enschede mentions that Felyx data isn't perfect: often rentals are missing. We respond and say that the cause is that Felyx only updates its data every 300 seconds instead of the 30 seconds that is in the specifications. We will contact Felyx again on this and ask for a solution, so that in the future the data feed is refreshed every 30 seconds and municipalities will have reliable data
| 2022-04-19 | Felyx attended our 'Introduction in MDS' meeting
| 2022-03-29 | Felyx emails: Enschede and Zwolle data is now shared with the CROW Dashboard. We confirm this is the case. Issue of March 8th is solved.
| 2022-03-28 | We email Felyx and ask: Can you enable Zwolle and Enschede, or give a planning/timeline?
| 2022-03-24 | Municipality of Enschede asks us again if Felyx data can be visible in the CROW Dashboard.
| 2022-03-10 | Felyx thanks us for signaling and informs that it will enable Zwolle and Enschede data.
| 2022-03-08 | We see that Zwolle and Enschede data are missing, while Felyx offers vehicles in these cities. We email Felyx and ask to include all NL data including Zwolle and Enschede.
| 2022-02-08 | Felyx emails: 2) 'Updating all data every 30s is difficult. But, `is_disabled` is realtime now. And we are looking if `is_reserved` can be close to realtime as well'  3) We are going to work on improving PROW mid February, expected delivery: beginning of March
| 2022-02-04 | Felyx replied to our email of 2021-01-24: 1) is fixed! Haarlem & Den Bosch are now present in the data feed. 2) Updating every 30s is difficult because external software fleetbird/NIU only updates every 5 minutes. 3) Felyx will start fixing PROW
| 2022-01-27 | At +- 9:10am the new Dashboard Deelmobiliteit was launched! We ended the rental of a Felyx bike in Amsterdam, but this bike did not show up immediately on the map. What did show up nearby the location: A Felyx scooter at 7:43am and 9:22am. Maybe it was one of these, presumably the last one. If so, it had a delay of 8 minutes.
| 2022-01-27 | At 8:00 am we noticed the update frequency was reverted(?) to 5 minutes
| 2022-01-26 | At 5:13pm we noticed the update frequency was +- 30 seconds
| 2022-01-24 | We asked Felyx by mail to 1) add Haarlem and Den Bosch 2) Update update frequency to <= 30s 3) Fix PROW
| 2022-01-24 | We asked Felyx by phone to update feed frequency from 5 minutes to every 30 seconds
| 2021-09-13 | Asked Felyx to update feed frequency, add data of Den Bosch+Haarlem, fix PROW and add vehicle type
