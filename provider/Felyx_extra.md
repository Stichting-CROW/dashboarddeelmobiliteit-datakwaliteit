# Data quality: Felyx - Additional info

## Don't include bikes that do not exist in public space

Felyx shares bikes with the Dashboard Deelmobiliteit that do not exist in public space.

Properties of this type of data are that it has a GPS location in public space, the property `is_disabled` is `1` and if you walk to the bike in real life, the bike is not there.

### Examples

```json
{
  "bike_id": "36fffebc-8969-4c4e-bf83-b4361694ac73",
  "lat": 53.24417,
  "lon": 6.530217,
  "is_reserved": false,
  "is_disabled": true
},
{
  "bike_id": "24f73fc6-0f0d-4a17-8b1a-ed7dd5fa17d2",
  "lat": 53.241435,
  "lon": 6.537152,
  "is_reserved": false,
  "is_disabled": false
},
{
  "bike_id": "ac260a2a-9a60-423a-92f0-ab70eb4d94e1",
  "lat": 53.220853,
  "lon": 6.539831,
  "is_reserved": false,
  "is_disabled": true
},
{
  "bike_id": "5d77bbc8-15e9-4c95-b48e-20bc15138f10",
  "lat": 53.215762,
  "lon": 6.558791,
  "is_reserved": false,
  "is_disabled": true
},
{
  "bike_id": "9f0fb985-62dc-40c0-9eb0-15244845131b",
  "lat": 53.236525,
  "lon": 6.579657,
  "is_reserved": false,
  "is_disabled": true
}

```

Bonus example: https://github.com/Stichting-CROW/dashboarddeelmobiliteit-datakwaliteit/issues/12#issuecomment-1020516588
