# ile-de-france-Stations

The data file provides information on the stations in the Ile-de-france region (mainly served by RERs, Metros, Trams, VALs, Transilien lines and Grandlines) in a json format.

Tuple include following information:

```
"line_code": String, representing the identifier of the line
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
### Other Info:
- The station names are represented in 2 ways. For the metro lines the name are in lower case while for all other modes it is in upper case
- The station names also have accented characters
- `underground = true` means that the station is underground. False represents the station is overground
- We have not included new proposed lines in Ile-de-France region
- More cities worldwide will be covered soon.
- The data contains 43 unique lines in the Ile-de-France region
	```
	{'_id': '3b', 'count': 4}
	{'_id': 'T3B', 'count': 18}
	{'_id': 'LIGNE L', 'count': 40}
	{'_id': '7b', 'count': 8}
	{'_id': 'GRD LIGNES', 'count': 33}
	{'_id': '6', 'count': 28}
	{'_id': 'LIGNE H', 'count': 50}
	{'_id': '10', 'count': 23}
	{'_id': 'LIGNE J', 'count': 49}
	{'_id': 'ORLYVAL', 'count': 3}
	{'_id': 'LIGNE U', 'count': 10}
	{'_id': '14', 'count': 9}
	{'_id': 'LIGNE K', 'count': 10}
	{'_id': 'LIGNE N', 'count': 35}
	{'_id': 'FUNICULAIRE MONTMARTRE', 'count': 2}
	{'_id': '2', 'count': 25}
	{'_id': '12', 'count': 29}
	{'_id': '11', 'count': 13}
	{'_id': 'LIGNE R', 'count': 24}
	{'_id': '5', 'count': 22}
	{'_id': 'T8', 'count': 17}
	{'_id': 'T11', 'count': 7}
	{'_id': '4', 'count': 27}
	{'_id': '8', 'count': 38}
	{'_id': '13', 'count': 32}
	{'_id': '7', 'count': 38}
	{'_id': '9', 'count': 37}
	{'_id': '3', 'count': 25}
	{'_id': 'CDGVAL', 'count': 5}
	{'_id': '1', 'count': 25}
	{'_id': 'RER E', 'count': 22}
	{'_id': 'T1', 'count': 37}
	{'_id': 'T2', 'count': 24}
	{'_id': 'T5', 'count': 16}
	{'_id': 'LIGNE P', 'count': 36}
	{'_id': 'T6', 'count': 21}
	{'_id': 'T3A', 'count': 25}
	{'_id': 'T7', 'count': 18}
	{'_id': 'RER A', 'count': 46}
	{'_id': 'RER B', 'count': 47}
	{'_id': 'RER C', 'count': 84}
	{'_id': 'T4', 'count': 11}
	{'_id': 'RER D', 'count': 59}
	```
for the above, (if you are using mongodb you can execute):
	```
	collection.aggregate(pipeline=[{'$group' : {'_id':'$line', 'count':{"$sum":1}}}])
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
