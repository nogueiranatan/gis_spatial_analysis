# 🌿 BioBlitz Biodiversity Spatial Analysis

![BioBlitz Heatmap](images/final_heatmap.png)

## Project Overview

This project analyses biodiversity observations collected through the iNaturalist platform during Griffith University BioBlitz events. Using GIS, the project identifies spatial patterns in citizen science observations to understand where biodiversity records are concentrated and to support future biodiversity surveys and event planning.

The analysis is conducted using observations from the Griffith University Nathan Campus.

---

## Objectives

- Visualise the spatial distribution of biodiversity observations.

- Identify observation hotspots across the study area.

- Demonstrate GIS techniques for analysing citizen science datasets.

- Produce clear cartographic outputs for ecological interpretation.

---

## Study Area

**Location:** Griffith University Nathan Campus, Brisbane, Queensland, Australia

---

## Data

| Dataset | Source |

|---------|--------|

| iNaturalist observations | iNaturalist export |

| Observation points | Imported into QGIS |

---

## Methodology

### 1. Import Biodiversity Observations

Observation records were extracted from iNaturalist for the Griffith University Nathan Campus study area and imported into QGIS as a point layer.

---

### 2. Create Analysis Grid

A fishnet grid with a spatial resolution of **25 × 25 metres** was generated to divide the study area into equal-sized analysis units.

---

### 3. Aggregate Observations

The **Join Attributes by Location (Summary)** tool was used to count the number of observation points (FIDs) intersecting each grid cell.

This produced an observation count for every grid cell, allowing observation density to be compared across the campus.

---

### 4. Create Observation Density Map

Graduated symbology was applied to the observation count field to visualise observation density.

Higher observation counts were represented using darker colours, producing a heatmap that highlights biodiversity observation hotspots across the campus.

---

## Results

The resulting heatmap reveals areas where citizen scientists recorded the greatest number of biodiversity observations, providing an initial assessment of sampling intensity across the campus.

This map forms the foundation for future analyses, including:

- Temporal distribution of observations

- Threatened species mapping

- BioBlitz versus non-BioBlitz observations

- Participant contribution analysis

---

## Skills Demonstrated

- GIS data management

- Vector spatial analysis

- Fishnet/grid creation

- Spatial joins

- Summary statistics

- Heatmap visualisation

- Cartographic design

- QGIS workflow development

---

## Software

- QGIS, iNaturalist, Excel
