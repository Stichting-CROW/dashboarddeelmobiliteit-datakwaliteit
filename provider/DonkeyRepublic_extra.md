# Data quality: Donkey Republic - Additional info

## Don't include bikes that do not exist in public space

Donkey Republic shares bikes with the Dashboard Deelmobiliteit, that do not exist in public space.

Properties of this type of data is that it has a GPS location in public space, the property `is_disabled` is `1` and if you walk to the bike in real life, the bike is not there.

### Example: 4 non-existing bikes in Utrecht inactive for >100 days 

In Utrecht there're multiple bikes inactive for > 100 days, with property `is_disabled=1`.

![img](https://user-images.githubusercontent.com/899234/129565481-6c80b483-aea7-432c-9700-a042228a84c4.jpg)

![img](https://user-images.githubusercontent.com/899234/129565583-5dd8448d-c231-44c5-8981-fe15aa4b02ab.png)

```json
{
  "bike_id": "7274",
  "is_disabled": 1,
  "is_reserved": 0,
  "lat": 52.080645,
  "lon": 5.1248324
},

{
  "bike_id": "7285",
  "is_disabled": 1,
  "is_reserved": 0,
  "lat": 52.080645,
  "lon": 5.1248324
},

{
  "bike_id": "7286",
  "is_disabled": 1,
  "is_reserved": 0,
  "lat": 52.080645,
  "lon": 5.1248324
},

{
  "bike_id": "7287",
  "is_disabled": 1,
  "is_reserved": 0,
  "lat": 52.080645,
  "lon": 5.1248324
},

```

## Request @DonkeyRepublic

Please make sure that bikes that are not in public space, are not offered in the data feed.

NOTE: Bikes that are disabled and _exist_ in public space, should still be offered with the correct GPS location and `is_disabled=1`.
