<p align="center">
  <img src="https://craton.sfo2.cdn.digitaloceanspaces.com/media/img/branding/hero/moss-hero.png" alt="logo" width="300px">
</p>

# The Flux Data

***Earthquake event data & random number data***

A verification resource created for research described in Quake Works [_The Flux_](https://flux.quake.works).

## Repository Layout

It is pretty intuitive but here is a little map so you don't have to click around too much :thumbsup:

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
|    |
|    |----\ random_org
|    |    |---\txt
|    |    |    |- randomOrg-10k-mrk-20190219_01.txt
|    |    |    |- randomOrg-10k-mrk-20190219_02.txt
...  ...  ...  \- LOTS OF TXT FILES...
|    |    |- randOrg-mrk-check.csv
|    |    \- readme.md
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

## Copyright

### Random Data Copyright

The data obtained from the [RANDOM.ORG](https://www.random.org/) website used and posted here with kind permission. :100:

It should be understood that number sets generated by PHP and MS Excel are technically **[pseudo-random](https://www.random.org/analysis/).** True random data requires a cryptographic element that cannot be reversed engineered. As PHP and Excel are discreet systems, their output is insecure. **Pseudo-random numbers are still chaotic in *output*** and a one-to-one comparison between the true random numbers gained from [RANDOM.ORG](https://www.random.org) and the pseudo-random data shows no statistical difference in the chaotic output as it pertains to this project.

### General Copyright

The data contained in this repository that I generated is released under the [MIT license](LICENSE), which roughly means: free to reuse with reference in your work, but the code is "As Is" status. [Peruse](LICENSE). :point_left:

### Seismic Event Data Copyright

The information downloaded from the USGS [API service](https://earthquake.usgs.gov/fdsnws/event/1/) was obtained freely under their [Public Release of Information policy](https://www.usgs.gov/information-policies-and-instructions/public-release-information). Copyright for this information is under the [Public Domain](https://www.usgs.gov/information-policies-and-instructions/copyrights-and-credits) and [no warranty](https://www.doi.gov/disclaimer) is implied or expressed on their part or mine.


# What Next...

<p align="center">
    <a href="https://quake.works">
        <img src="https://craton.sfo2.cdn.digitaloceanspaces.com/media/img/branding/btn-web.svg" width="120px">
    </a>
    <a href="https://twitter.com/quakeyeager">
        <img src="https://craton.sfo2.cdn.digitaloceanspaces.com/media/img/branding/btn-twitter.svg" width="120px">
    </a>
    <a href="https://github.com/jakeYeager">
        <img src="https://craton.sfo2.cdn.digitaloceanspaces.com/media/img/branding/btn-github.svg" width="120px">
    </a>
    <a href="https://paypal.me/quakeyeager?locale.x=en_US">
        <img src="https://craton.sfo2.cdn.digitaloceanspaces.com/media/img/branding/btn-paypal.svg" width="120px">
    </a>
</p>
