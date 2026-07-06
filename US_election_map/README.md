# US Presidential Election Results by County (2020)

![outputs](outputs/us_election_2020.png)

### Objective
Develop a county-level choropleth map of the 2020 US Presidential Election that visualises both the winning political party and the strength of each county’s majority vote. The map uses expression-driven opacity to encode vote-share percentage, allowing areas with stronger electoral majorities to appear more visually prominent.

### Data
MIT Election Data and Science Lab (MEDSL)  
US county boundary shapefiles

### Methods

Data preparation:
- Joined county-level election results to county boundary polygons using a common identifier.
- Verified attribute integrity prior to visualisation.
  
Data classification: 
- Symbology categorization: Classified counties by winning political party using the QGIS Expression Builder.
CASE
WHEN "per_gop" >  "per_dem" THEN 'R'
WHEN "per_dem" > "per_gop" THEN 'D' 
END
- Applied categorical symbology using red (Republican) and blue (Democratic).
- Created an expression-driven opacity field so counties with larger winning vote percentages appear darker, while more competitive counties appear lighter.
CASE
WHEN "per_dem" > "per_gop" THEN "per_dem" *100	
WHEN "per_gop" > "per_dem" THEN "per_gop" *100
END

Print layout:
- Created a custom opacity legend to communicate vote-share intensity, where darker colours indicate larger winning margins and lighter colours indicate closer contests.
- Applied consistent typography, legend hierarchy and map composition to improve readability.
-   
### Key Findings

- Democratic-majority counties are concentrated along the West Coast, the Northeast, and around major metropolitan areas.
- Republican-majority counties occupy a much larger geographic area, particularly across rural regions of the United States.
- Opacity successfully communicates the strength of electoral support, distinguishing strong partisan counties from more competitive areas.
- Limitations: The map illustrates spatial voting patterns rather than population distribution. Because counties vary greatly in population, geographic area should not be interpreted as representing the number of votes cast.

### Skills Demonstrated

* QGIS
* Spatial data integration
* Attribute joins
* Expression Builder
* Rule-based symbology
* Expression-driven opacity
* Choropleth cartography
* Print Layout design
* Cartographic communication
* Data visualisation

