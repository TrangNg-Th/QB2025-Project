# QB2025-Project
Study on the effect of climate change on biodiveristy of macrozoobenthos in the Baltic sea

> **Note**: This is R project for biodiversity BIOL Z620 in Spring 2025

---

## Table of Contents
- [QB2025-Project](#qb2025-project)
  - [Table of Contents](#table-of-contents)
    - [Data variables](#data-variables)
  - [Evironemental variables](#evironemental-variables)
  - [Environmental Variables](#environmental-variables)
    - [Data sources](#data-sources)
  - [Data preparation](#data-preparation)
  - [Codes](#codes)
  - [Updates](#updates)


### Data variables
## Evironemental variables
| **Variable**                      | **Unit**       | **Why Important**                                                                                           |
## Environmental Variables

| **Variable**                                  | **Unit**       | **Why Important**                                                                                           |
|-----------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------|
| **Bot. Depth**                                | m             | Represents the bottom depth of the water, which influences habitat conditions and species distribution.   |
| **Secchi Depth**                              | m             | Measures water clarity and light penetration, affecting photosynthesis and primary production.              |
| **Depth (ADEPZZ01_ULAA)**                     | m             | Indicates the sampled water depth,|
| **Temperature (TEMPPR01_UPAA)**               | °C            | Affects metabolic rates, chemical reactions, and species distribution in aquatic ecosystems.               |
| **Salinity (PSALPR01_UUUU)**                  | unitless      | Determines species composition, affects water density, and influences ocean circulation.                   |
| **Oxygen (DOXYZZXX_UMLL)**                    | ml/l          | Essential for marine life                                 |
| **Phosphate (PHOSZZXX_UPOX)**                 | µmol/l        | Key nutrient for phytoplankton growth                      |
| **Total Phosphorus (TPHSZZXX_UPOX)**          | µmol/l        | Includes all phosphorus forms, indicating overall nutrient availability      |
| **Silicate (SLCAZZXX_UPOX)**                  | µmol/l        | Necessary for diatom growth, influencing primary production and food web dynamics.                         |
| **Nitrate + Nitrite (NTRZZZXX_UPOX)**         | µmol/l        | Indicator of nutrient load and potential eutrophication, impacting oxygen levels.                          |
| **Nitrate (NTRAZZXX_UPOX)**                   | µmol/l        | Major nitrogen source for phytoplankton growth                             |
| **Nitrite (NTRIZZXX_UPOX)**                   | µmol/l        | Intermediate in nitrogen cycling                   |
| **Ammonium (AMONZZXX_UPOX)**                  | µmol/l        | Readily available nitrogen source for phytoplankton           |
| **Total Nitrogen (NTOTZZXX_UPOX)**            | µmol/l        | Sum of all nitrogen forms, reflecting overall nutrient availability and ecosystem productivity.            |
| **Hydrogen Sulfide (H2SXZZXX_UPOX)**          | µmol/l        | Indicates anoxic conditions; toxic to marine life and influences redox chemistry.                          |
| **pH (PHXXZZXX_UUPH)**                        | pH units      | Affects carbonate chemistry, species survival, and ocean acidification.                                    |
| **Total Alkalinity (ALKYZZXX_MEQL)**          | mEq/l         | Buffers pH changes and is essential for carbonate system stability.                                        |
| **Chlorophyll a (CPHLZZXX_UGPL)**             | µg/l          | Proxy for phytoplankton biomass and primary productivity, indicating ecosystem health.                     |



### Data sources
[Environmental data from NCEI]( https://www.ncei.noaa.gov/access/world-ocean-database-select/bin/dbsearch.pl ) 
[Macrozoobenthos data from OBIS](https://www.eurobis.org/toolbox/en/download/occurrence/dataset/601)



---

## Data preparation
1. **Data Collection**: Collect data from NCEI and OBIS.
   - Download data from OBIS using the following query ![alt text](image.png)
   - Download data from ICES using the query [here](https://www.ices.dk/data/dataset-collections/Pages/default.aspx)
      - Geographic range: Baltic Sea ![alt text](image-4.png)
      - Temporal range: 1980-2005 
## Codes
- `0.dataprep.ipynb` : Data preparation and cleaning for macrozoobenthos and environmental data.
- `1.analysis.ipynb` : Data analysis and visualization.
---

## Updates
- **2025-01-30**: Looked at the dataset `sps_macrozoobenthos_timeseries.csv`, and found that not all sites are sampled every year. There is a big difference between sites. -> Suggestion : Take the 10 most sampled sites and look at the data.

- **2025-02-01**:
  - Create notebook `0.dataprep.ipynb` for data preparation and cleaning.
  - Create SyS matrices for macrozoobenthos data. After filtering, only 3 sites have data for almost all years and for all environmental variables.
  - Create environmental data matrices for the same 3 sites over years
  