# `/data`

## Raw data: `/data/raw`

`/data/raw` contains unprocessed data as downloaded from the IHME Global Burden of Disease website.

> [!IMPORTANT]
> GBD data is used under the [IHME Free-of-Charge Non-commercial User Agreement](https://www.healthdata.org/about/ihme-free-charge-non-commercial-user-agreement), which forbids commercial use of the data. Contact IHME for commercial uses.

`IHME-GBD_2019_DATA-737d59c6-1.csv`: Summary Exposure Values (SEVs) for heat, cold and ambient air pollution.

`IHME-GBD_2019_DATA-fd70d168-1.csv`: death rates and percentages where neonatal preterm birth was the cause of death and ambient air pollution was an identified risk.

Columns for both include:

- `measure`: either `Summary exposure value` or `Deaths`
- `location`: the country
- `sex`: `Both`
- `age`: the age group, or `Age-standardized`
- `cause`: the cause of death (only in the latter file)
- `rei`: the identified risk
- `metric`: SEV, `Percentage` or `Rate`
- `year`: the year of observation
- `val`: the central estimate of the value
- `upper`: the upper bound of the estimated value
- `lower`: the lower bound of the estimated value

## Processed data

GBD data processed into a variety of shapes.

`agestd-allsex-allcause-pollutiontemp-sev.csv`: a tidied version of the raw SEV data, still in "long" format and using original country names.

`agestd-allsex-allcause-pollutiontemp-sev-byrisk.csv`: the SEV data widened to put air pollution, heat and cold alongside each other. ISO2 codes have been added and country names have been standardised using the `{countrycode}` package.

`agestd-allsex-allcause-pollutiontemp-sev-wide.csv`: the SEV data widened further to put every year's air pollution, heat and cold central estimates alongside each other. Upper and lower bounds are dropped. This file is shaped especially for Datawrapper, so there are spacer columns between each group of risk columns that include CSS in the header. ISO2 codes have been added and country names have been standardised using the `{countrycode}` package.

`lt28days-allsex-preterm-pollution-deathrate100k.csv`: the data on deaths from preterm birth and air pollution, lightly tidied. Uses the original country names.
