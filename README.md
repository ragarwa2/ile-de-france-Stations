# ile-de-france-Stations

The data file provides information on the stations in the Ile-de-france region (mainly served by RERs, Metros, Trams, VALs, Transilien lines and Grandlines) in a json format.

Tuple include following information:

```
"line_code": String, representing the identifier of the line
"line": String, representing line number
"stop_id": Integer, representing identifier of the station
"stop_name":String, representing name of the station
"coordinates": Array, represnting apatial coordinates of the station in the Longitude, Latitude format
"underground": Boolean, representing if the station is underground or overtheground
```

example tuple:
```json

{
	"line_code":"7-107089",
	"coordinates":[2.377267200151936,48.81593076304922],
	"stop_id":642,
	"underground":true,
	"line":"7",
	"stop_name":"Pierre Curie"
}

```

### Authors
- [Rachit Agarwal](https://github.com/ragarwa2/)
- [Shaan Chopra](https://github.com/shaan15)

### Licence
CC

### Acknowledgement
We Acknowledge Stif for providing the [data](https://opendata.stif.info/explore/dataset/emplacement-des-gares-idf/information/).

### Reporting Issues
In case you find any issue in our labels for underground and overtheground please report it by opening an issue.
