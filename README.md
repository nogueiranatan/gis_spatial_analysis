# Natan's GIS Spatial Analysis Portfolio

## 🗺️ Choropleth Map - Median Household Income by County (USA)

![Choropleth map](Choropleth_Medianhouseholdincome.png)

### Objective

Analyse spatial distribution of median household income across US cities.

### Data

- US Department of Agriculture (2019)

### Methods

Join: 
- Combined xml-spreadsheet data (join layer) of median household income with vector layer of counties (target layer).

Data classification: 
- Choropleth classification (natural breaks), separated by US$ 10,000 increments (excluding first and last tiers). 

Print layout:
- Addition of two maps in addition to continental U.S. to improve visibility of the states of Hawaii and Alaska.
- Alteration of Coordinate Reference Systems (CRS) for the additional two maps to improve projection (EPSG: 3338 / ESRI: 102007)

### Key Findings

- Clear spatial clustering of high-income areas in coastal cities
- MAUP (Modifiable Areal Unit Problem) is a limitation. Economic data is susceptible to discrepancies depending on definition of county boundaries.
