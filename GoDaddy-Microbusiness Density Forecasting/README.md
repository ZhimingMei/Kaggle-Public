# GoDaddy - Microbusiness Density Forecasting

## Introduction

## Target
Predict monthly microbusiness density in a given area.

## Dataset
> All the information collected from the data description of [competition webpage].

- 'train.csv':  

**row_id**; **cfips** (a unique identifier for each country); **country_name**; **state_name**; **first_day_of_month**; **microbusiness_density** (microbusinesses per 100 people over the age of 18 in the given country. This is the **target** variable. The population figures used to calculate the density are on a two-year lag to the pace of update provided by the US census bureau. 2021 density figures are calculated by using 2019 population figures, etc.); **active** (the raw count of microbusiness in the country)

- 'census_starter.csv': examples of useful columns from the Census Bureau's American Community Survey. **All fields have a two year lag to match what information was available at time a given microbusiness data update was published**

**pct_bb_\[year\]** (The percentage of households in the country with access to broadband of any type); **cfips**; **pct_college_\[year\]** (The percent of the population in the county over age 25 with a 4-year college degree); **pct_foreign_born_\[year\]** (The percent of the population in the county born outside of the United States); **pct_it_workers_\[year\]** (The percent of the workforce in the county employed in information related industries); **median_hh_inc_\[year\]** (The median household income in the county)


## Evaluation Method
We use **symmetric mean absolute percentage error**, which is an accuracy measure based on percentage error.

$\text{SMAPE} = \frac{100\%}{n}\Sigma_{t=1}^n \frac{|F_t-A_t|}{(|A_t|+|F_t|)/2}$

where, $A_t$ is the actual value and $F_t$ is the forecast value.

## Progress Notes

### Ideas

### Remarks


[competition webpage]: https://www.kaggle.com/competitions/godaddy-microbusiness-density-forecasting/data
