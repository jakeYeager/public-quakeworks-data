# Seismic Events Data

The was downloaded from the USGS for your convenience **though ideally you should [create your own](https://earthquake.usgs.gov/earthquakes/search/) independently.** It is possible I have consistency issues. 

### Collection Query Specs

Primary goal for creating the seismic event population was to create the largest possible volume of entities within a continuous period. The following constraints were applied according the the data source [USGS API service](https://earthquake.usgs.gov/fdsnws/event/1/):

- **location agnostic** (latitude and longitude values were set to their respective extremes)
- **exclusively earthquakes** (no other seismic event types were allowed, i.e. quarry blasts, nuclear explosions)
- **allowed magnitude of only >M3.9**
- **time period between January 1, 1940 and December 31, 2018** (1940-01-01T00:00:00Z to 2018-12-31T23:59:59Z)

## CSV Schema

The data is recorded in CSV files and organized in the following column schema (with headers):

| id     |    date   | mag | year |  mo | mrk | day | hour | depth |
| ------ | :-------: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| string | timestamp | int |  int | int | int | int |  int |  int  |

- ID is included for validation purposes
- Timestamp has been formatted to be recognized by spreadsheet applications
- Magnitude has been reduced to it's leading whole integer (as in the research it is treated more as a reference 'tag' than measurement).
- Time elements have been extracted from timestamp upon database export.
- Depth is provided gratis :wink:
