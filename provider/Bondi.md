# Data quality: Bondi

## Data quality status

Last updated at 2024-06-26.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ✅ GBFS 1.0
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ❌

Status: 🟡 Usable though needs improvement

## Improvements to make

### Support MDS `/vehicles`

Start using MDS `/vehicles` end point wich gives better data quality and makes it possible to share vehicle types as well.

## Logs

| Updated    | Description
| ----       | ---
| 2022-07-09 | 🎉 We added Bondi to the Dashboard with GBFS 1.0. For the longer term we still need to try to add MDS `/vehicles` instead of GBFS, because vehicle types are supported in that standard. For now we setted up a default vehicle type as Bondi has only electric bicycles at the moment.
| 2022-07-05 | wunder mobility suggests to use GBFS 1.0 for now.
| 2022-06-30 | wunder mobility answers: 'I've opened a change request to our product team to evaluate a change on that and let you know about our decision.'
| 2022-06-30 | The feed works. Although all vehicles are split up in batches of 20. We ask: 'It would be really nice for us to not use pagination. Paging would add a lot of latency. Is there a possibility to setup a higher limit so that we can retreive all the vehicles instead of only 20 per api call?'
