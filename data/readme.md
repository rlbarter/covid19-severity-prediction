# full data sources

Only need to download these if you want to rerun the scraping / preprocessing pipeline.

## from google drive
- **[hrsa data](https://data.hrsa.gov/data/download)**: get df_renamed.pkl from [here](https://drive.google.com/open?id=1OfeUn8RcOfkibgjtuuVt2z9ZtzC_4Eq5) and put into proper directory: `data/hrsa/data_AHRF_2018-2019/processed/df_renamed.pkl`
    - provides demographics, income estimates, some mortality rates, hospital numbers, and more (all per county)
- **[voting data](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/VOQCHQ)**: download `county_voting_processed.pkl` from [here](https://drive.google.com/drive/u/2/folders/1OfeUn8RcOfkibgjtuuVt2z9ZtzC_4Eq5) and put into proper directory `data/voting/county_voting_processed.pkl`
    - ratio of votes in each county of democrat : republican in 2016 election
- **[diabetes data](https://gis.cdc.gov/grasp/diabetes/DiabetesAtlas.html#)**: DiabetesAtlasCountyData.csv from [here](https://drive.google.com/open?id=1dfV8kEzVtMVzJKRyHVam9gsGq-WnvyHm) and put into proper directory: data/diabetes/DiabetesAtlasCountyData.csv
    - diabetes rate per county
- **[respiratory disease data](http://ghdx.healthdata.org/record/ihme-data/united-states-chronic-respiratory-disease-mortality-rates-county-1980-2014)**: `IHME_USA_COUNTY_RESP_DISEASE_MORTALITY_1980_2014_NATIONAL_Y2017M09D26.XLSX` from [here](https://drive.google.com/drive/u/2/folders/1OfeUn8RcOfkibgjtuuVt2z9ZtzC_4Eq5) and place at `data/respiratory_disease/`
    - respiratory disease mortality rate per county
- **[icu beds data](https://khn.org/news/as-coronavirus-spreads-widely-millions-of-older-americans-live-in-counties-with-no-icu-beds/)**: download `icu_county.csv` from [here](https://drive.google.com/drive/u/2/folders/1OfeUn8RcOfkibgjtuuVt2z9ZtzC_4Eq5) and put into proper directory `data/icu/icu_county.pkl`
    - number of icu beds per county
- **[heart disease data](https://nccd.cdc.gov/DHDSPAtlas/?state=County)**: heart_disease_mortality_data.csv from [here](https://drive.google.com/open?id=1glMZ7l6UxYTjBUvvFNV7Hu8QXC-j5q3C) and put into proper directory: `data/cardiovascular_disease/heart_disease_mortality_data.csv`
- **[stroke data](https://nccd.cdc.gov/DHDSPAtlas/?state=County)**: stroke_mortality_data.csv from [here](https://drive.google.com/open?id=1ozVEjSGaQcRfJYnicKvEimKpAD3umI7o) and put into proper directory: `data/cardiovascular_disease/stroke_mortality_data.csv`
- **[mortality data](https://wonder.cdc.gov/cmf-icd10.html)**: Compressed Mortality, 2012-2016.txt from [here](https://drive.google.com/open?id=1xdscgVTtM30WuR3YUYVTdgC4IbTwdFZ_) and put into proper directory: `data/mortality/Compressed Mortality, 2012-2016.txt`; mortality rates (per year and per county) are also available by age group
- **countyFIPS**: in `data_hospital_level/processed/02_county_FIPS.csv.`
    - county identifier


## through scripts
- **confirmed cases + deaths - [usafacts data](https://usafacts.org/visualizations/coronavirus-covid-19-spread-map/) (updated daily)**: using script at `data/usafacts/download_usafacts_data.sh`
- **[medicare data](https://www.cms.gov/Research-Statistics-Data-and-Systems/Statistics-Trends-and-Reports/Chronic-Conditions)**: using script at `data/medicare/download_medicare_data.sh`
- **[tobacco-use data](https://www.countyhealthrankings.org/explore-health-rankings/measures-data-sources/county-health-rankings-model/health-factors/health-behaviors/tobacco-use/adult-smoking)**: using script at `data/tobacco/download_tobacco_use_data.sh`i

## hospital-level data
- [list of academic hospitals](https://www.cms.gov/OpenPayments/Downloads/2020-Reporting-Cycle-Teaching-Hospital-List-PDF-.pdf)
- **private hospital-level data**: available in slack channel, rename to `04_hospital_level_info_merged_website.csv` put into `data_hospital_level/processed/04_hospital_level_info_merged_website.csv`
    - also can download some of the datasets using the scripts in the data_hospital_level directory