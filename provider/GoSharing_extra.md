# Data quality: GO Sharing - Additional info

Below I document incorrect data in the GO Sharing MDS feed.

## P7B7, 2022-10-21 12:24

**SUMMARY: Scooter staat wel in de feed, maar met incorrecte gegevens**

Deze scooter (ID: P7B7 oftewel 12128) staat in Rotterdam in de buurt van de Hofplein-rotonde, maar staat volgens de feed in Vlaardingen volgens de feed.

Het batterijpercentage is 0. Het voertuig is niet zichtbaar in de GO Sharing app. De status in de MDS feed is: available.

Dit zijn 2 fouten in de feed.

```json
{
  "provider_id": "bc9fbe6a-a3c0-11ec-b909-0242ac120002",
  "provider_name": "GoSharing-Netherlands",
  "device_id": "00000000-0000-1000-a000-000000012128",
  "vehicle_id": "P7B7",
  "vehicle_type": "moped",
  "propulsion_types": [
    "electric"
  ],
  "last_event_time": 1666342599108,
  "last_vehicle_state": "available",
  "last_event_types": [
    "trip_cancel"
  ],
  "last_event_location": {
    "type": "Feature",
    "properties": {
      "timestamp": 1666342599108
    },
    "geometry": {
      "type": "Point",
      "coordinates": [
        4.34977341,
        51.90610886
      ]
    }
  },
  "current_location": {
    "type": "Feature",
    "properties": {
      "timestamp": 1666342562664
    },
    "geometry": {
      "type": "Point",
      "coordinates": [
        4.34977341,
        51.90610886
      ]
    }
  },
  "battery_pct": 0.0
}
```
