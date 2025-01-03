# Identifying Impacts of Extreme Weather Blackouts in Houston, TX

## About

This study aims to identify the impacts of a series of extreme winter storms by estimating the number of homes in the Houston metropolitan area that lost power. Additionally, it will investigate whether these impacts were disproportionately felt among certain populations.
- Mapping power outages utilizing VIIRS data
- Performing raster operations such as masking, buffering, and spatial joins 
- Visualizing statistics through plots
  
## Repository Structure
```bash
blackout-houston
├── README.md
├── .gitignore
├── blackout-houston.qmd
├── Rmd/Proj files
└── data
    ├── gis_osm_roads_free_1.gpkg
    ├── gis_osm_buildings_a_free_1.gpkg
    ├── ACS_2019_5YR_TRACT_48_TEXAS.gdb
    └── VNP46A1
        ├── VNP46A1.A2021038.h08v05.001.2021039064328.tif
        ├── VNP46A1.A2021038.h08v06.001.2021039064329.tif
        ├── VNP46A1.A2021047.h08v05.001.2021048091106.tif
        └── VNP46A1.A2021047.h08v06.001.2021048091105.tif
```
## Data
All datasets have been downloaded and organized within the data folder in this repository. The Visible Infrared Imaging Radiometer Suite (VIIRS) datasets are specifically located in the VNP46A1 subfolder for easy access. Since Houston lies on the border of tiles h08v05 and h08v06, two tiles were downloaded for each date.

- VNP46A1.A2021038.h08v05.001.2021039064328.tif: Tile h08v05, collected on 2021-02-07
- VNP46A1.A2021038.h08v06.001.2021039064329.tif: Tile h08v06, collected on 2021-02-07
- VNP46A1.A2021047.h08v05.001.2021048091106.tif: Tile h08v05, collected on 2021-02-16
- VNP46A1.A2021047.h08v06.001.2021048091105.tif: Tile h08v06, collected on 2021-02-16

The roads and buildings datasets were obtained from OpenStreetMap via [Geofabrik](https://download.geofabrik.de). These datasets were processed into a GeoPackage containing only roads and houses in the Houston metropolitan area.

The ACS_2019_5YR_TRACT_48.gdb file is an ArcGIS file geodatabase. You can explore its contents using the `st_layers()` function from the `stars` R package.

All code for querying data and accessing specific layers is provided in the blackout-houston.qmd file.

## References

NASA. (2021). VNP46A1--5000 VIIRS dataset for 2021-02-07 and 2021-02-16 within the region -96.5, 30.5, -94.5, 29. NASA EOSDIS. Retrieved from https://ladsweb.modaps.eosdis.nasa.gov/search/order/4/VNP46A1--5000/2021-02-07..2021-02-07,2021-02-16..2021-02-16/NB/-96.5,30.5,-94.5,29

OpenStreetMap contributors. (n.d.). Planet OSM. Retrieved from https://planet.openstreetmap.org

U.S. Census Bureau. (2019). TIGER/Line shapefiles: 2019 ACS data. Retrieved from https://www2.census.gov/geo/tiger/TIGER_DP/2019ACS/

## Acknowledgements

This repository was created for a final project related to the course EDS 223: Geospatial Analysis & Remote Sensing.

This course is an academic requirement for the Master of Environmental Data Science (MEDS) program at the Bren School of Environmental Science & Management, University of California, Santa Barbara.
