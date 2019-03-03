# RANDOM.ORG

The purpose of this research was to test real data against randomly generated "white noise" data. As pseudo-random generators offered an efficient means to this end, and no cryptographic characteristics were needed, they were employed to the bulk of the comparative tasks. True random numbers were obtained *only* as a [control check](https://www.random.org/analysis/) against the pseudo-random batches to insure that suitable chaotic outcomes are possible **and** were being generated across populations. Read [their documentation](https://www.random.org/randomness//) for specifics on how the true random generation is executed.

To make this control, 400,000 random numbers were generated via the RANDOM.ORG integer web page. Batches of choices between 1 and 16 were gained in 10k per HTTP request, by sets of 5 x2000. There was a daily limit imposed by IP so 10k batches had to be complied. Full txt versions of the raw page output is available, as well as a unified, single-column CSV `randOrg-mrk-check.csv`.

Thanks to RANDOM.ORG for permission to post their service output here! :100:
