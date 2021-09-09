# Data quality: GO Sharing - Additional info

## Don't include mopeds that do not exist in public space

GO Sharing shares mopeds with the Dashboard Deelmobiliteit that do not exist in public space.

Properties of this type of data are that it has a GPS location in public space, the property `is_disabled` is `1` and if you walk to the bike in real life, the moped is not there.

### Example 1: GO Sharing mopeds standing still for > 100 days

There're many vehicled that are parked for > 100 days.

![img](https://i.imgur.com/YsLWp0K.png)

These vehicle _are_ listed in the that GO Sharing shares with the Dashboard Deelmobiliteit.

An example of such a vehicle is this one:

```json
{
  "bike_id": "3898",
  "lat": 52.050289154052734,
  "lon": 4.322021484375,
  "is_reserved": 0,
  "is_disabled": 1,
  "rental_uris": {}
}
```

The problem here is that this vehicle is not present in public space, but is still available in the feed.

The [PROW specifications](https://github.com/openmobilityfoundation/mobility-data-specification/blob/main/provider/README.md#mobility-data-specification-provider) for determining if a vehicle should be included in the datafeed or not mention the following.

A vehicle should only be included if:

- The vehicle is in public space, available and not rented out
- The vehicle is in public space and reserved
- The vehicle is in public space and disabled
- The vehicle is in public space and defect

If a vehicle is reserved, disabled or defect, the vehicle status must be included as described in the data standard.

If a vehicle is _not present in public space_ (because it's stolen), the vehicle should be excluded from the data feed.

In this case the vehicles that are not in public space, should not be listed as `is_disabled=1`, but should be removed from the feed.

### Example 2: Mopeds moved by trucks

Regularly  mopeds are shared that are not in public space, but moved by a truck.

Examples:

![img](https://user-images.githubusercontent.com/899234/129569775-7da5f806-2bf6-4e98-875d-e1185f8b7097.jpg)

![img](https://user-images.githubusercontent.com/899234/129570049-fb26fff9-9f7f-43cf-bd49-2587e2bc284d.jpg)

![img](https://user-images.githubusercontent.com/899234/129920884-342a2966-be3e-4191-8b3c-294dd9cfe308.png)

![img](https://user-images.githubusercontent.com/899234/129921008-b605bfc9-9021-4853-805f-6e58248ca4ae.png)

