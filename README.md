# Identifying Impacts of Extreme Weather Blackouts in Houston, TX

## About

This study aims to identify the impacts of a series of extreme winter storms by estimating the number of homes in the Houston metropolitan area that lost power. Additionally, it will investigate whether these impacts were disproportionately felt among certain populations.
- Mapping power outages utilizing VIIRS data
- Performing raster operations such as masking, buffering, and spatial joins 
- Visualizing statistics through plots

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

All the data has been downloaded and stored in the data folder. The VIIRS data files can be accessed within a separate subfolder.

## References

Bureau, U. C. (2024, October 22). American Community Survey (ACS). Census.gov.

Geofabrik Download server. Geofabrik Download Server. (n.d.).

NASA. (n.d.). Level-1 and Atmosphere Archive & Distribution System Distributed Active Archive Center - LAADS DAAC. NASA.

## Acknowledgements

This repository was created for a final project related to the course EDS 223: Geospatial Analysis & Remote Sensing.

This course is an academic requirement for the Master of Environmental Data Science (MEDS) program at the Bren School of Environmental Science & Management, University of California, Santa Barbara.
