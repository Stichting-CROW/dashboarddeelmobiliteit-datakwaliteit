# Data quality: Greenwheels

## Data quality status

Last updated at 2026-11-24.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ via CHECK MDS-feed (sinds 2026-11-18)
| Updated <= 30s?             | ✅ via CHECK
| Correct PROW?               | ❔
| All NL data?                | ❔ zone-based voertuigen te controleren
| Includes vehicle type?      | ✅
| Offers service areas        | ❌

Status: 🟡 Bruikbaar via CHECK-feed; aparte Greenwheels-feed bestaat niet meer

## Improvements to make

- Controleren of zone-based Greenwheels-auto's ook in de CHECK-feed / op de kaart staan

## Logs

| Updated    | Description
| ----       | ---
| 2026-11-18 | 🎉 Greenwheels en CHECK zijn één bedrijf geworden. Vanaf 18 november staan de Greenwheels-deelauto's in de CHECK MDS-feed
| 2026-11-10 | ⏳ Melding: niet alle Greenwheels-auto's lijken op de site te staan; mogelijk ontbreken zone-based voertuigen. Te controleren
| 2025-11-18 | 🎉 Data is weer aanwezig sinds 18 november 12:56. Onafgesloten parkeerperiode's van voor 1 november zijn handmatig beeindigd op datum/tijd 2025-10-24 13:14.
| 2025-10-24 | 🐛 Data is afwezig sinds 24 oktober 13:13
| 2022-05-03 | Greenwheels answers: we are reading into the topic and are in exploratory phase for the solution design. We can't be more precise or give a testing date. As soon as we can, we will let you know.
| 2022-05-03 | We answer the questions and ask: is implementation of this /vehicles MDS endpoint on your roadmap, and when do you expect to deliver the first test version of this feed?
| 2022-04-20 | Greenwheels went through the documentation and sends us questions.
| 2022-04-19 | We did an online technical briefing on what is MDS, how to offer a MDS feed and how to integrate with CROW Dashboard
| 2022-02-28 | Greenwheels wants to start with MDS in the beginning of Q2, with support of CROW. We will plan a meeting / demo: "How to offer a MDS feed".
