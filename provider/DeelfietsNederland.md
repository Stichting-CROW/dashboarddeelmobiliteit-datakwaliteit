# Data quality: Deelfiets Nederland

## Data quality status

Last updated: 2026-10-07.

| **Quality check**           | **Quality**
| --                          | -- |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ✅
| Offers service areas        | ❌

Status: 🟢 Perfect

## Improvements to make

- Geen

## Logs

| Updated    | Description
| ----       | ---
| 2026-09-16 | 🎉 Deelfiets Nederland heeft deelfietsen die incorrect op de kaart stonden aangepast/verwijderd, en een procedure geimplementeerd die een dergelijke situatie in de toekomst voorkomt. We zien dat veel lang-stilstaande voertuigen inderdaad van de kaart verdwenen zijn.
| 2026-09-08 | We hebben Deelfiets Nederland gevraagd te controleren of de data in het DD een juist beeld geeft van de beschikbare voertuigen ven Deelfiets Nederland. Aanleiding was dat er veel gebieden zijn waarin voertuigen staan die nooit gebruikt worden, en dat 1 voertuig in de feed staat die zelfs al 3 jaar niet is gebruikt
| 2024-01-09 | Deelfiets Nederland meldt: "Vanaf maandag 15 januari worden de voormalig KeoBike fietsen opgenomen in onze datafeed zoals we die momenteel hebben met het Dashboard Deelmobiliteit. Per die datum mag de huidige KeoBike feed worden gestopt en die fietsen die daar eventueel nog aan gekoppeld zijn worden verwijderd."
| 2023-09-04 | 🐛->✅ Sinds +- 2022-11-07 heeft Deelfiets Nederland de oude GBFS-feed uitgefaseerd. Echter bleven in totaal 6 voertuigen uit die oude feed op de Dashboard Deelmobiliteit kaart staan. Vandaag hebben we deze niet-meer-bestaande voertuigen uit de database verwijderd. Het betreft deze voertuigen: `4082e09f-c140-4ee6-a5be-31849b487301`, `128e096e-29cb-429d-9fda-2f159356b4fd`, `0d64ac39-02b2-4f66-9c45-42320dfae40b`, `ed07079d-887b-408b-b11c-1655316e737b`, `26ebcdbc-93b4-4641-a3ff-4ca99fe2a309`.
