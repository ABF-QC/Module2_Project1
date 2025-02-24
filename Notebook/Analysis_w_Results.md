# Climate Weather Station Inventory Analysis

## Objective
The goal is to analyse the climate weather stations over the province of Quebec. During the analysis, we will find a list of climate stations that are available over a period of at least 30 years, in order to be used in another project later on to produce climate trends.

The goal is to analyze Environment and Climate Chnage Canada (ECCC) climate weather station inventory over the province of Quebec. For a weather station to be used to produce climatological data and trend, reports need to be available over a minimum of 30 consecutive years.

---
### During the analysis,

1. The weather station will be categerorized by the reports frequency (hourly, daily and/or montlhy reports)
    * An interactive map will be produced to see the location of each station in the inventory list.(see ../graph/StationReportFrequency.html)
      * Pertinent station information will be available interactively once the station is clicked on.
      * Different basemap is available to see various things of interest. These things combined can help to chose the most representative station for a city or point of interest.
        * Roads
        * Population Density
        * Vegetation type
    * An interactive pie chart will be produced to see the percentage of station and count of station in each category. (see ../graph/PieChart_StationCountbyReportFrequency.html)
2. The weather stations that could be used to produced climatological data and trend will be found. In other words, weather stations that are available over a period of at least 30 years, will be found.
    * A table containing all the weather station satisfying the climatological threshold will be produced. (see ../graph/Table_StationAvailableOver30years.html)
3. The number of years in service will be calculated for each weather station in order to evaluate its disbribution.
    *An interactive bar plot classifying the number of years in service will be produced. (see ../graph/BarChart_StationYearsinService.html)
4. Weather station clustering. Weather station can change name, ID, location (slightly) through the years, but still be considered to represent the same area. Thus, in order to have more weather stations satisfying the climatological service life threshold of ≥ 30 yrs, we often cluster weather stations together that share similarities (ie. same name, same location, within a certain distance from each other).
   * A simple clustering of weather station based on the name and coordinates will be applied.
    * A list of the gained weather stations (satifying the climatological threshold ≥ 30 yrs) from the clustering will be produced.
    * An interactive map will be produced to see the location of individual stations and the clustered weather stations.(see ../graph/StationClusteringByCoords.html)
      * Pertinent station information will be available interactively once the station is clicked on.
      * Different basemap is available to see various things of interest. These things combined can help to chose the most representative station for a city or point of interest.
        * Roads
        * Population Density
        * Vegetation type
---

### Data source
Here is the data source used for the Climate Weather Station Inventory Analysis
- [ECCC datamart climate data](https://dd.weather.gc.ca/climate/)  

---

### Analysis domain


At the moment, the climate weather stations were analyzed over the Quebec's province only.


![image info](pictures/image.png)