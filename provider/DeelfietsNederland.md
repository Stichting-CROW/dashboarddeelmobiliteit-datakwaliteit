# Data quality: Deelfiets Nederland

## Data quality status

Last updated: 2022-09-05.

| **Quality check**           | **Quality**
| --                          | -- |
| Uses data standard?         | ✅ GBFS
| Updated <= 30s?             | ✅
| Correct PROW?               | ✅
| All NL data?                | ✅
| Includes vehicle type?      | ❌ ✅ (feed 1: no, feed 2: yes)

Status: 🟡 Usable though needs improvement

## Improvements to make

- Add all places in 1 feed
- Add vehicle_type_id for every vehicle, in both feeds

## Logs

| Updated    | Description
| ----       | ---
| 2022-09-05 | Since July 8th no feed outage has happened, which is good. We still have to fix [this issue](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/issues/24) so we get support for two feeds that run simultaneously.
| 2022-06-08 | Today and yesterday we got an feed timeout. This explains the many rentals in the database on these two days.
| 2022-05-18 | We enabled both GBFS feeds again. If no timeouts happen, data will be stored well. If timeouts happen, a lot of rentals will be stored in the database.
| 2022-05-16 | We disabled the new GBFS feed, as it seemed to give some [problems](https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/issues/24). As soon as we investigated this, we activate the feed again (or give feedback to the provider).
| 2022-04-19 | We activated the new GBFS feed. Now two GBFS feeds are running simultaneously.
| 2022-04-19 | Deelfiets Nederland emails: 'We have a feed ready for you on the new platform. We can keep the old feed running on the existing URL. Simultaneously we run the new feed with most of the locations of Deelfiets Nederland. PS The new feed supports vehicle_type_id.'
| 2022-03-28 | We email: "We are happy if we can have the data of Deelfiets Nederland in the Dashboard soon. For the NS+IenW 'landelijke pilot deelfietsen op stations' this is obligated. Q: If the new feed is ready, can we keep the old feed as long as the locations of the old feed are not migrated to the new feed yet? So can we use 2 GBFS feeds until the end of 2022?"
| 2022-03-20 | Deelfiets Nederland emails: "We are migrating to a new backend. At this moment the following location use the old backend: P+R Hoogkerk Groningen, Kampen, bewaakte fietsenstalling Lubeckplein Zwolle. Most locations use the new backend, that doesn't offer a GBFS feed yet.<br /><br />We can offer a GBFS feed based on the new backend. We can support `vehicle_types` there as well. The development team expects this can be realised end of April 2022.<br /><br />In the GBFS feed based on the new backend these locations will be included: Ommen, Dalfsen, all locations in Friesland, Arnhem, Nijmegen, Enschede and most locations in Zwolle. The locations of the old feed will be gone from the moment the new feed is activated. We expect to migrate the locations from the old to new feed in the end of 2022."
| 2022-03-11 | We asked Deelfiets Nederland to include all NL vehicles in the data feed (asked before in September 2021)
| 2022-03-10 | We got an email notifying that Zwolse Deelfiets and Deelfiets Nederland are not shared, but they should. (Both brand names are part of the same company. Started as Zwolse Deelfiets, then follow up as "Deelfiets Nederland" with operations in Kampen + Friesland as well).
| 2022-03-08 | Municipality of Enschede mentions: data Deelfiets Nederland is not shared, but should be
| 2021-09-09 | Asked Deelfiets Nederland to offer all NL data and add vehicle type
