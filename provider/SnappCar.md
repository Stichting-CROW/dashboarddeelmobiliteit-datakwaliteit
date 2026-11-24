# Data quality: SnappCar

## Data quality status

Last updated at 2026-11-24.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ MDS 2.0
| Updated <= 30s?             | ❌ elk uur
| Correct PROW?               | ❔
| All NL data?                | ✅
| Includes vehicle type       | ✅
| Shares service areas        | ❌

Status: 🟡 Usable though needs improvement

## Improvements to make

### Update more frequently (every 30s)

To be compliant with the quality requirements, the data feed should be updated every 30s

### Fix rentals and duplicate vehicles

Verhuringen worden amper geregistreerd. Bij aanbod komen soms dubbele voertuigen voor. Te controleren/oplossen.

## Logs

| Updated    | Description
| ----       | ---
| 2026-11-18 | 🐛 SnappCar noemt aankomende week de MDS-feed aan te passen, zodat verhuurde voertuigen uit de MDS-feed verdwijnen of de juiste voertuigstatus krijgen
| 2026-11-11 | 🐛 Verhuringen worden amper geregistreerd. Bij aanbod komen vreemde dingen voor (bijv. 2× hetzelfde voertuig). Te controleren
| 2026-11-05 | We've added the MDS 2.0 Vehicles datafeed offered by SnappCar. Data is refreshed every hour. `vehicle_type` is car, `propulsion_types` is `electric` or `combustion`
