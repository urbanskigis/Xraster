# Xraster
Xraster is a tool designed for scientists and specialists to analyze multidimensional data describing the marine environment and climate. This data is provided by various organizations and scientific institutions (e.g., the European Union's Copernicus Programme) in the NetCDF format, which allows for the creation, access, and dissemination of array-oriented data. The array represents a grid on the Earth’s surface, with variables assigned to each cell. Depending on spatial factors, the grid can be 2-dimensional (e.g., sea surface temperature) or 3-dimensional (e.g., water temperature with depth). An additional dimension characterizing this data is time, resulting in data sets that are typically 3-dimensional (x, y, and time) or 4-dimensional (x, y, z, and time). Geographic Information Systems (GIS) are the primary tools for spatial data analysis.

Xraster is embedded as a plugin in QGIS, enabling two-way integration for data processing. The plugin uses raster and point layers created in QGIS and generates data (raster layers and text data) that can be used within the program, creating a simple Multidimensional GIS. Xraster is based on the functionalities of the Python module xarray, providing an interface to this module, allowing the entire data processing and analysis workflow to be carried out without the need for programming. 

Videos:

Xraster (users guide) - coastal waters monitoring      https://youtu.be/MVE8LaGd9uM 

........data for video: cmems_mod_bal_phy_anfc_P1D-m_ZG23_11_24_10.nc, ZG2_zones4.tif


Xraster (users guide) - climate analysis    https://youtu.be/btqZyZaCcj8

........data for video: opadPL_1950_2023.nc, temp_maxPL_1950_2023.nc, temp_srPL_1950_2023.nc, PLmask_woj.tif, puck_bay_coast1cell.tif, watershad_mask_KW.tif  


Data download for videos:   https://nc-marbefes.iopan.pl/nextcloud/s/qBWXn5TmYqkmPww  
