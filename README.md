s3_catch
================

Catchment-scale Sentinel-3 processing

Purpose
================
This package is a python framework supporting the user in processing Sentinel-3 netcdf files from SARvatore GPOD (https://gpod.eo.esa.int/) and SciHub (https://scihub.copernicus.eu/). 
The framework and equations are detailed in:

Kittel, C. M. M., Jiang, L., Tøttrup, C., and Bauer-Gottwein, P.: Sentinel-3 radar altimetry for river monitoring – a catchment-scale evaluation of satellite water surface elevation from Sentinel-3A and Sentinel-3B, Hydrol. Earth Syst. Sci. Discuss., https://hess.copernicus.org/preprints/hess-2020-165/, in review, 2020.

This project contains functionalities including
- crop_raster: extract subsets of larger raster files to speed up processing 
- s3_subset_ncdf: subset SciHub NetCDF files to speed up processing'
- s3_preprocessing: Extract all relevant l1b and l2 observations for virtual stations or individual tracks (floodplain processing)
- s3_evaluate
- s3_utils: contains functions used by the other scripts to process the sentinel-3 files

Read model file 
Extraction of network information, including drainage pattern, catchment and order of stream reaches.


Dependencies
======================
To follow the full workflow from the HESSD paper, additional processing in e.g. QGIS might be required. It is recommended to ensure the following dependencies are installed:


- datetime
- os
- sys
- numpy
- struct
- itertools
- decimal
- unittest

- netCDF4
- geopandas
- GDAL


It is expected that the user has the following shapefiles and rasterfiles:
- DEM 
- Water occurrence map
- Virtual stations shapefile



Getting started
======================

A test dataset is provided along with the plugin, containing the files required for use, as developed for the HESSD article.

Copyright (C) 2020 Cecile M. M. Kittel (ceki@env.dtu.dk) and Technical University of Denmark (www.dtu.dk)
