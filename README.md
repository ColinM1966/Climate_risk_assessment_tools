
# Climate Risk Assessment tools

A series of tools to conduct a climate risk assessment for an area of interest (AoI) supplied as either a polygon or a point with a defined buffer. 

## General information 
### Supported spatial inputs include:
- GeoPackage polygon layers
- ESRI Shapefiles
- KML files
- point locations, converted to assessment areas using a user-defined buffer

### The workflow:
- Reads and validates the input spatial data;
- Repairs invalid geometries;
- Converts buffered points or multiple polygons into a single assessment unit;

### Required R packages:
- sf
- terra
- exactextractr
- dplyr
- purrr
- readr
- tidyr


# Coastal Inundation Exposure Assessment

This R workflow assesses coastal inundation exposure for any user-defined area of interest.It uses exactextractr to calculate inundated area and percentage exposure for the eight return periods (1, 2, 5, 10, 25, 50, 75, and 100 year inundation events). It creates a cropped rasters for the AOI
where: 1 = inundated, 0 = not inundated and -9999 = NoData). It exports a results and a summary CSV reports.  



Update the input file, layer name, point-buffer distance where required, raster directory, and output paths in the user settings section before running the script.
