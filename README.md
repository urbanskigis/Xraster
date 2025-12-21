# Xraster
<b>About</b>

Xraster is a tool designed for scientists and specialists to analyze multidimensional data describing the marine environment and climate. This data is provided by various organizations and scientific institutions (e.g., the European Union's Copernicus Programme) in the NetCDF format, which allows for the creation, access, and dissemination of array-oriented data. The array represents a grid on the Earth’s surface, with variables assigned to each cell. Depending on spatial factors, the grid can be 2-dimensional (e.g., sea surface temperature) or 3-dimensional (e.g., water temperature with depth). An additional dimension characterizing this data is time, resulting in data sets that are typically 3-dimensional (x, y, and time) or 4-dimensional (x, y, z, and time). Geographic Information Systems (GIS) are the primary tools for spatial data analysis.
Xraster is embedded as a plugin in QGIS, enabling two-way integration for data processing. The plugin uses raster and point layers created in QGIS and generates data (raster layers and text data) that can be used within the program, creating a simple Multidimensional GIS. Xraster is based on the functionalities of the Python module xarray, providing an interface to this module, allowing the entire data processing and analysis workflow to be carried out without the need for programming.
<br><br>
<b>Install</b>
<br><br>Operating system:   Windows 10 (version 2009), 11    (at this time only)

The installation process of Xraster in QGIS follows these steps:

    • You need to download the packaged plugin  xraster_gis_?.zip  from the   website:   https://github.com/urbanskigis/Xraster  to any directory.
    • Open QGIS 3.xx (minimum version 3.20) - QGIS should be  installed using OSGeo4W installer with selected packages QGIS and GDAL (at least)
    • Open "Plugin" menu from the top bar
    • Select "Manage and Install Plugins...
    • Go to "Install from ZIP"
    • Select  xraster_gis_?.zip 
    • Click install
      
Since the plugin requires additional Python libraries that are not installed by default, if they are not found, a message will be displayed, <b>ModuleNotFoundError</b>

In such a case, you should:

    • Go to the C: /OSGeo4W directory where the OSGeo installer has installed QGIS
    • Run OSGeo4W.bat
    • Check with pip list packages installed   ( C:/OSGeo4W>pip list )

  You need to install the packages:<b> xarray, netCDF4, h5netcdf, scipy (NEW in version 4) and Cartopy </b> using the following four commands executed in sequence:
 
<br>
C:/OSGeo4W>pip install xarray
<br>
C:/OSGeo4W>pip install netCDF4
<br>
C:/OSGeo4W>pip install h5netcdf
<br>
C:/OSGeo4W>pip install scipy
<br>
C:/OSGeo4W>pip install Cartopy

<br><br>
<b>Functionalities (basic)</b><br>
<br>
Data import - Input of NetCDF data consisting of 2D raster grids with a time dimension. <br><br>
Subset - Creates a subset of a selected variable for a specified range of dimensions: spatial coordinates, time, and depth. <br><br>
Calculate - Recalculates the current subset variable using a Python expression.<br> <br>
Filtering - Filter of the data subset using comparison and logical operators. <br><br>
Time Summary - Calculates temporal statistics from surface data (x, y, time) and from point data (z, time).<br><br>
Spatial Summary - Calculates statistics from all available data (subset, mask, filtering) at a specified time.<br>

Extract - Extracts raster data at specified points; outputs text file. 

Cross -  Generates time series of cross-sections from 4D subset.

‍‍‍Group by time -  Divides data into groups for defined time periods and  calculates specified statistics for each group.

‍‍‍Clip - Clips the area of interest from NetCDF data.

Merge - Merging NetCDF files by time or by  variables. 

Data Export - Exports the current data subset to a NetCDF file. 
<br><br>
<b>Manual and Tutorial</b><br><br>
The manual  <b>Xraster_QGIS_Plugin_user_manual_EN_04.pdf</b>  and the tutorial  <b>Xraster_tutorial_v3.pdf</b> together with the accompanied data, are available.  <br><br>
<b>Contribute</b><br><br>
Jacek Urbański<br><br>
<b>Licence</b><br><br>
GNU General Public License v2.0

<b>Additional Resources</b>

Videos:
<br><br>
Xraster (users guide) - coastal waters monitoring      https://youtu.be/MVE8LaGd9uM 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;data for video: cmems_mod_bal_phy_anfc_P1D-m_ZG23_11_24_10.nc, ZG2_zones4.tif

<br>
Xraster (users guide) - climate analysis    https://youtu.be/btqZyZaCcj8

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;data for video: opadPL_1950_2023.nc, temp_maxPL_1950_2023.nc, temp_srPL_1950_2023.nc, PLmask_woj.tif, 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;puck_bay_coast1cell.tif, watershad_mask_KW.tif  
<br>
Baltic eutrophisation with Xraster           https://youtu.be/Q4nnglSsanA

<br>
How to Create a Mask for Xraster            https://youtu.be/y7LF3ptTy3A 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;data for video: Baltic_subbasins2.zip

<br>
QGIS Analysis of Xraster Zonal Statistics Output       https://youtu.be/_E8teYpUJts

<br> Xraster analyzes the thermohaline structure and ice extent in the Arctic.      https://youtu.be/8YJOPwgh6Qs 

<br> Xraster analyzes the climate changes (air temperature) in Antarctica.          https://youtu.be/QfBCvPbj7iU              

<br><br>
Data download for videos:   https://nc-marbefes.iopan.pl/nextcloud/s/qBWXn5TmYqkmPww  
