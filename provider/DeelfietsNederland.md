# Data quality: Deelfiets Nederland

## Data quality status

Last updated: 2024-06-26.

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
| 2024-01-09 | Deelfiets Nederland meldt: "Vanaf maandag 15 januari worden de voormalig KeoBike fietsen opgenomen in onze datafeed zoals we die momenteel hebben met het Dashboard Deelmobiliteit. Per die datum mag de huidige KeoBike feed worden gestopt en die fietsen die daar eventueel nog aan gekoppeld zijn worden verwijderd."
| 2023-09-04 | 🐛->✅ Sinds +- 2022-11-07 heeft Deelfiets Nederland de oude GBFS-feed uitgefaseerd. Echter bleven in totaal 6 voertuigen uit die oude feed op de Dashboard Deelmobiliteit kaart staan. Vandaag hebben we deze niet-meer-bestaande voertuigen uit de database verwijderd. Het betreft deze voertuigen: `4082e09f-c140-4ee6-a5be-31849b487301`, `128e096e-29cb-429d-9fda-2f159356b4fd`, `0d64ac39-02b2-4f66-9c45-42320dfae40b`, `ed07079d-887b-408b-b11c-1655316e737b`, `26ebcdbc-93b4-4641-a3ff-4ca99fe2a309`.
