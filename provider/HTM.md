# Data quality: HTM

## Data quality status

Last updated: 2022-04-11.

| **Quality check**           | **Quality**
| --                          | --          |
| Uses data standard?         | ❌ MDS
| Updated <= 30s?             | ➖
| Correct PROW?               | ➖
| All NL data?                | ➖
| Includes vehicle type?      | ➖

Status: 🔴 Unusable

## Improvements to make

### Use data standard

At the moment HTM offers a GBFS feed having incorrect data.

HTM should offer the data using one of the standards: MDS, GBFS or TOMP. Preferably MDS.

### Add vehicle type

🆕 The operator should communicate what kind of vehicle it's reporting. 

Since GBFS 2.1 there's a field, `vehicle_type_id`, that defines what kind of vehicle is offered.

To implement this, you can use these documentation pages: 

1. Offer [vehicle_types.json](https://github.com/NABSA/gbfs/blob/master/gbfs.md#vehicle_typesjson-added-in-v21)
2. In free_bike_status.json, add property [vehicle_type_id](https://github.com/NABSA/gbfs/blob/master/gbfs.md#free_bike_statusjson)

As values you can use the [latest](https://github.com/NABSA/gbfs/pull/370) standard definition for mopeds:

- name: `HTM fiets type 1`,
- vehicle_type_id: `htm_type_1`
- form_factor: `moped`
- propulsion_type: `electric`
- wheel_count: `2`

To see an example, see page 2 of [this document](https://docs.google.com/document/d/1P_oDBnFvr9qzo0_5YbnrCDYptFQV9ZUOJGfi8ACD1GE/edit?usp=sharing).


## Logs

| Updated    | Description
| ----       | ---
| 2022-04-05 | Joyride replies to the mail of 2022-04-04: "We understand your point of view. We are determining the requirements for updating the MDS to version 1.2, which will happen in the comming months. Any further updates will be shared with you as soon as they are available." "We will also give an update when our planning is becoming more detailed."
| 2022-04-04 | We reply HTM: "GBFS should work, _if_ the ID's do not rotate. But because the IDs in Joyride GBFS-feed do rotate, this doesn't give us a solution that works (we have been in contact with Joyride about this many times). MDS /vehicles is a standard that focusses specifically on monitoring, and therefor in this standard it sais that the IDs should not rotate. This is the reason that we ask for the MDS /vehicles implementation now, as GBFS has not be implemented to the specification we require for more than half a year already."
| 2022-04-04 | HTM replies: "How does Dashboard Deelmobiliteit differ from other apps? In the HTM app we use the GBFS feed of Joyride and in this app we see exactly where our HTM bikes are. Would this GBFS feed be an option that works for you as well?"
| 2022-04-04 | We contact HTM: "To be able to get data in the Dashboard Deelmobiliteit we need a specific dataset, [the MDS /vehicles endpoint](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/provider/README.md#vehicles). Joyride does not support this endpoint at the moment, while this is a requirement for The Hague. Joyride has to implement this end point or HTM instruct to do so."
| 2022-04-04 | We reply Joyride: "For three of Joyride's customers (Bondi, Baqme and HTM) the feed is a hard requirement to be able to get a permit in multiple municipalities within the Netherlands. We are trying for a long time to get this feed working for these three operators. How we can make sure that it gets implemented at your side within reasonable time? As far as we know it shouldn’t be really difficult because the /vehicles is pretty similar to the /free-bike-status endpoint of GBFS, with the big difference that static vehicle_id’s are guaranteed. 
| 2022-04-04 | Joyride replies: "We checked your GBFS query from our end and it works fine. Hereby we send you example commands. As for MDS: we don't have the /vehicles end point. Let me know if you need any more information from our side."
| 2022-03-30 | We ask for a status update. HTM sends Joyride a reminder. We do this as well: "Since February we try to get access to the MDS feed of Joyride. On March 24th Sven sent an email mentioning that we cannot access the feed, with the question: can you give us information so we can access the feed? Could you please connect us with the development team, so we get an example of how to reach the MDS feed of Joyride/HTM?"
| 2022-03-24 | Joyride sais it's going to check with the development team and it will come back on this.
| 2022-03-24 | We tested credentials, /vehicles doesn't seems to work. /trips returns an error stating 'Your request is with missing details. Try again', we reviewed the MDS documentation and don't know what is missing. Contacted Joyride again about this problem. 
| 2022-03-21 | Joyride sends credentials.
| 2022-03-18 | HTM gives permission and we ask Joyride if they provide /vehicles endpoint.
| 2022-03-17 | We got reply per email: HTM needs to give permission to share MDS URL + token.
| 2022-03-11 | We reply per email: HTM does not know the MDS feed URL and asks to contact Joyride directly. Therefor the same question again: Could you please send us the MDS feed URL?
| 2022-03-03 | Joyride replies per email: Please ask HTM for the URL.
| 2022-02-22 | We email Joyride: Do you have a MDS feed available for us?
| 2022-01-25 | HTM sends a feed URL that has 'mds' in the URL path but isn't MDS
| 2022-01-24 | We email HTM: Could you ask your development partner if a MDS feed can be shared?
| 2022-01-19 | We email HTM: 'The data is in the Dashboard, but is not of high quality. We expect dynamic IDs are used instead of static IDs. The best option would be to offer a MDS data feed'.
| 2022-01-19 | HTM emails: any updates?
| 2021-12-22 | The HTM data that was shared by spreadsheet is not equal to the HTM data shared by the GBFS feed. We disable the feed, share our findings with HTM and ask to improve/fix the GBFS feed
| 2021-12-10 | HTM sent the amount of trips for November 24th to December 10th. We will do a comparison
| 2021-12-10 | We tested the feed. There're static IDs now, which is good. We see that there're less trips than park events though. We asked HTM for the amount of HTM trips for November 24th to December 10th
| 2021-10-26 | HTM sent a new GBFS URL. We will test this
