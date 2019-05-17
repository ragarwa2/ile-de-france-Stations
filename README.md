# MetroStations

The data files provides information on the stations in various cities (for now: Ile-de-france region (RERs, Metros, Trams, VALs, Transilien lines and Grandlines) and Lyon (metro)) in a json format.

Tuple usually include following information:

```
"line_code": String, representing the identifier of the line (some cities do not contain this field)
"line": String, representing line number
"stop_id": Integer, representing identifier of the station
"stop_name":String, representing name of the station
"coordinates": Array, representing sapatial coordinates of the station in the Longitude, Latitude format
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
	
### Author
- [Rachit Agarwal](https://github.com/ragarwa2/)


### Licence
CC-By


### Reporting Issues
In case you find any issue in our labels for underground and overtheground please report it by opening an issue.
