# Data quality: Lime

## Data quality status

Last updated at 2021-09-02.

| **Quality check**           | **Quality**
| --                          | --                  |
| Uses data standard?         | ❌ GBFS rotated IDs
| Updated <= 30s?             | ✅
| Correct PROW?               | ❔
| All NL data?                | ✅
| Includes vehicle type?      | ✅

Status: 🔴 Unusable

## Improvements to make

### Use static vehicle IDs

At the moment LIME uses rotated IDs. LIME should use static IDs instead. At the moment the feed is unusable.

## Logs

|Updated    |Description
|----       |---
|2021-09-14 |Asked Lime to implement static vehicle_ids
