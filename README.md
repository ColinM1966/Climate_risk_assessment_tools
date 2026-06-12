





<b>Coastal Inundation Exposure Assessment

This R workflow assesses coastal inundation exposure for any user-defined area of interest.

Supported spatial inputs include:
GeoPackage polygon layers
ESRI Shapefiles
KML files
point locations, converted to assessment areas using a user-defined buffer

The workflow:
reads and validates the input spatial data;
repairs invalid geometries;
converts buffered points or multiple polygons into a single assessment unit;
uses exactextractr to calculate inundated area and percentage exposure;
processes 1-, 2-, 5-, 10-, 25-, 50-, 75-, and 100-year inundation return periods;
exports long, wide, and summary CSV reports;
creates cropped and masked inundation rasters where:
1 = inundated
0 = not inundated
-9999 = NoData

Required R packages
sf
terra
exactextractr
dplyr
purrr
readr
tidyr

Update the input file, layer name, point-buffer distance where required, raster directory, and output paths in the user settings section before running the script.
