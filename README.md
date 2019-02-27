<p align="center">
<img src="logo.png" style="width: 128px;">
</p>

# Quake Works Flux Data

_Earthquake data as well as datasets created by various random number generators_

A verification and utilization resource created from research described in the [QuakeWorks/Flux](https://flux.quake.works) site.

## Copyright and Disclaimers

### Random Data Copyright

The data contained in this repository that I generated is released under the [MIT license](LICENSE), which means: free to reuse with reference in your work, but the code is "As Is" status.

### Random Data Disclaimer

It is acknowledged and understood that almost all of the random number sets are **[pseudo-random](https://www.random.org/randomness/).** True random data requires a cyrptographic element that cannot be reversed engineered. That being said **pseudo-random numbers are still very chaotic** and a one-to-one comparison between the true random numbers gained from [RANDOM.ORG](https://www.random.org) and the pseudo-random datasets shows no statistical difference in the chaotic output as it pertains to this research project.

### Seismic Event Data Copyright

The information downloaded from the USGS [API service](https://earthquake.usgs.gov/fdsnws/event/1/) was obtained freely under their [Public Release of Information policy](https://www.usgs.gov/information-policies-and-instructions/public-release-information). Copyright for this information is under the [Public Domain](https://www.usgs.gov/information-policies-and-instructions/copyrights-and-credits) and [no warranty](https://www.doi.gov/disclaimer) is implied or expressed on their part or mine.

## Repository Layout

It is pretty intuitive but here is a little map so you don't have to click around too much :100:

```txt
\
---- \ quakes
|    |- quakes_1940-2018.csv
|    \- readme.md
|
---- \randoms
|    |----\ excel
|    |    |- erb-set1.csv
|    |    |- erb-set2.csv
|    |    |- erb-set3.csv
|    |    |- erb-set4.csv
|    |    |- erb-set5.csv
|    |    \- readme.md
|    |  
|    |----\ php_mtrand
|    |    |- mtr-set1.csv
|    |    |- mtr-set2.csv
|    |    |- mtr-set3.csv
|    |    |- mtr-set4.csv
|    |    |- mtr-set5.csv
|    |    \- readme.md
|    |  
|    |----\ php_rand
|    |    |- r-set1.csv
|    |    |- r-set2.csv
|    |    |- r-set3.csv
|    |    |- r-set4.csv
|    |    |- r-set5.csv
|    |    \- readme.md
|
|- .gitignore
|- LICENCE
\- README.md
```

## Generation Schema

Characteristics:

- Three random number generators were used to provide five "sets" of 416,102 entities to match a corresponding seismic event record.
- Each set contains six sample population "batches" which match the respective quantity of seismic event sample populations designated by magnitude ranges.
- Batches were generated independently, and are not subdivisions of a mass population.
- Each entity has three associated randomly generated "time value" number choice:
  + a "month" value (number between 1 - 12)
  + a "marker" value (number between 1 - 16)
  + and a "hour" value (number between 0 - 23)

A tree-view structure visualization would be as follows:

```txt
Generator "X"
 \
 - - - Set #1 (416,102 total entities)
 |      \
 |      | - - Batch 1 (333,857 entities): [month val] [marker val] [hour val]
 |      | - - Batch 2 (72,257 entities): [month val] [marker val] [hour val]
 |      | - - Batch 3 (8,950 entities): [month val] [marker val] [hour val]
 |      | - - Batch 4 (970 entities): [month val] [marker val] [hour val]
 |      | - - Batch 5 (63 entities): [month val] [marker val] [hour val]
 |      \ - - Batch 6 (5 entities): [month val] [marker val] [hour val]
 |      
 - - - Set #2 (416,102 total entities)
 |      \
 |      | - - Batch 1 (333,857 entities): [month val] [marker val] [hour val]
 |      | - - Batch 2 (72,257 entities): [month val] [marker val] [hour val]
 |      | - - Batch 3 (8,950 entities): [month val] [marker val] [hour val]
 |      | - - Batch 4 (970 entities): [month val] [marker val] [hour val]
 |      | - - Batch 5 (63 entities): [month val] [marker val] [hour val]
 |      \ - - Batch 6 (5 entities): [month val] [marker val] [hour val]
 |
 - - - Set #2 (416,102 total entities)
 |      \
 |        etc...
```
