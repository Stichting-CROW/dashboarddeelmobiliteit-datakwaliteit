# Data quality: TIER

## Data quality status

Last updated: 2022-02-17.

| **Quality check**           | **Quality**
| --                          | --      |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ❔
| All NL data?                | ✅
| Includes vehicle type?      | ✅

Status: 🟢 Perfect

## Improvements to make

None. All seems to work well now.

## Logs

| Updated    | Description
| ----       | ---
| 2022-02-17 | 🎉 We activated the new Amersfoort and Eindhoven feed
| 2022-02-09 | TIER emails GBFS feed URLs of Amersfoort and Eindhoven (and made our API key valid for using these feeds)
| 2022-02-07 | We ask to share GBFS feed URL and API key for Amersfoort and Eindhoven. We will load multiple individual feeds for now, instead of 1 feed for all of NL.
| 2022-01-24 | TIER emails and asks: 'Is it possible to process multiple seperate feeds instead of 1 feed for all places in NL?' We reply that best would be 1 feed, but for now we can do this.
| 2022-01-21 | TIER mentions that there's not 1 NL feed, but only individual feeds per city. "Providing one API link for all cities is more work and needs to be included later on the road map"
| 2022-01-10 | TIER pro-actively asks if Eindhoven and Amersfoort can be added as well. We reply: If these cities are added to to the existing GBFS (NL) feed, these are included automatically
| 2021-12-23 | 🎉 GBFS feed for TIER Utrecht is added!
| 2021-10-13 | From a legal side we are fine and can start working on the technical implementation together with CROW
