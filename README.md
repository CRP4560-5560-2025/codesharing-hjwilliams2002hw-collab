README – Story County Median Age by Sex Choropleth

 Author: Hunter Williams
 
 Date: December 2025
 
Purpose
 This project creates a graduated-color choropleth map showing the median age by sex for census tracts in Story County, Iowa. The workflow joins a cleaned CSV dataset to a GeoJSON boundary file and visualizes the results using ArcGIS Pro and a Python toolbox.
 
Data Sources
 CSV File:
 Story County Median Sex By Age Clean.csv
 Source: U.S. Census Bureau – ACS 5-Year Estimates
 Table: B01002 – Median Age by Sex
GeoJSON File:
 StoryCounty.geojson
 Source: ArcGIS Online / census boundary dataset
 Contains Story County census tract polygons.
 
Field Definitions
 Label (Grouping): Census tract identifier used for joining.
 Total: Numeric median age value for the selected sex category.
 Other fields: Added automatically by ArcGIS during processing.
 
Processing Steps
Cleaned the CSV so that:
Column 1 = Label (Grouping)
Column 2 = Total
All rows contain valid values
Loaded the GeoJSON file into ArcGIS Pro.
Added the cleaned CSV to the project.
Performed a join using:
GEOID (GeoJSON)
Label (Grouping) (CSV)
Applied graduated colors symbology using the Total field.
Exported the final output as Story_County_Output_File.
Created a Python toolbox that automates:
Selecting CSV and GeoJSON
Converting GeoJSON
Joining data
Applying display settings
Creating a matplotlib graph
Saving outputs
Coordinate System
 The GeoJSON uses WGS84 (EPSG:4326) unless otherwise noted. ArcGIS Pro reprojects as needed.

Notes
The dataset contains only one sex category. Additional columns are needed if mapping male and female separately.
Ensure the join fields remain text to prevent GEOID mismatches.
The dataset contains only one sex category. Additional columns are needed if mapping male and female separately.
Ensure the join fields remain text to prevent GEOID mismatches.
