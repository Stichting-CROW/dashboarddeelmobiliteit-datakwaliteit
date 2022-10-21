# Data quality: Felyx - Additional info

Below I document incorrect data in the Felyx GBFS feed.

## dd32..54d5, 2022-10-21 12:24

**SUMMARY: Voertuig staat in GBFS feed, maar staat niet in publieke ruimte**

Dit voertuig, **dd328068-ab0b-4d28-9ed6-bd8a0abf54d5**, staat in de GBFS feed, maar kunnen we niet vinden in de publieke ruimte.

De status van dit voertuig is in de feed: is-disabled. Dit betekent dat het in de openbare ruimte zou moeten staan, maar dat het niet beschikbaar is voor verhuur. Het voertuig staat er echter niet.

Kunnen jullie nakijken wat hier mis is? Misschien is het iets wat vaker voorkomt, bij alle voertuigen in de feed.

```
{
  "bike_id": "dd328068-ab0b-4d28-9ed6-bd8a0abf54d5",
  "lat": 51.92525,
  "lon": 4.47709,
  "is_reserved": false,
  "is_disabled": true
},
```
