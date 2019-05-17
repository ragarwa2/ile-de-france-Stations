# Lyon Metro Stations

The data file provides information on the stations in the lyon region (mainly served by Metro) in a json format.

Tuple include following information:

```
"line": String, representing line number
"stop_name":String, representing name of the station
"coordinates": Array, representing sapatial coordinates of the station in the Longitude, Latitude format
"underground": Boolean, representing if the station is underground or overtheground
```

example tuple:
```json

{
	"coordinates":[4.8291954, 45.7530404],
	"underground":true,
	"line":"A",
	"stop_name":"Ampère - Victor Hugo"
}

```
### Other Info:
- Some staion names are repeated as they serve different lines on different platforms. Example:
	```
	{'_id': 'Hôtel de Ville - Louis Pradel', 'count': 2}
	{'_id': 'Saxe - Gambetta', 'count': 2}
	```

- The station names also have accented characters
- `underground = true` means that the station is underground. False represents the station is overground
- We have not included new proposed stations in Lyon region
- The data contains 4 unique lines in the Lyon region
	```
	{'_id': 'A', 'count': 14}
	{'_id': 'B', 'count': 10}
	{'_id': 'C', 'count': 5}
	{'_id': 'D', 'count': 15}
	```
for the above, (if you are using mongodb you can execute):
	```
	collection.aggregate(pipeline=[{'$group' : {'_id':'$line', 'count':{"$sum":1}}}])
	```
	
### Authors
- [Rachit Agarwal](https://github.com/ragarwa2/)

### Licence
CC-By

### Acknowledgement
We acknowledge openstreetmap for providing the [data](https://www.openstreetmap.org).

### Reporting Issues
In case you find any issue in our labels for underground and overtheground please report it by opening an issue.
