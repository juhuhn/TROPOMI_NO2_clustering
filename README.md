# TROPOMI_NO2_clustering

[![DOI](https://doi.org/XXXX)](https://doi.org/XXXX)

Jupyter Notebook containing Python codes and results for TROPOMI NO2 clustering.
It is an end-to-end notebook with demonstration of the spatio-temporal data preprocessing and clustering on TROPOMI NO2 measurement.
For brevity of presentation, the notebook displays the analysis result tested on the Red Sea region.

## Preliminary
Before running the notebook, one needs to download the [TROPOMI NO2 column density dataset](https://data.4tu.nl/articles/_/16943725).

## Schematic representation
![schematic representation](scheme.png)

## Input Data
The used data are listed below.

1. TROPOMI NO2 data

    For the regridded TROPOMI NO2 dataset, please refer to the following link: [TROPOMI NO2 column density dataset](https://data.4tu.nl/articles/_/16943725).
   
    - The dataset contains the processed data of open-source level-2 TROPOMI NO2 measurements on the Mediterranean Sea area, the Red Sea, and the Indian Ocean, publicly available via the Copernicus S5P hub (https://s5phub.copernicus.eu) and retrieved by TROPOspheric Monitoring Instrument (TROPOMI) on board the Copernicus Sentinel-5 Precursor satellite.
    - The dataset is regridded, day-averaged, and provided by Airbus Defence and Space Netherlands. That is, all irregularly gridded L2 data is interpolated on a regular grid defined in World Geodetic System 1984 (WGS84). In addition, if the same measurement pixel is available with valid data from a different point in time on the same day, the result contains multiple contributes of the same weight but with different scaled values, such that time averaging is performed as well.
    - The dataset has four variables: nitrogendioxide_tropospheric_column; nitrogendioxide_tropospheric_column_precision; nitrogendioxide_slant_column_density; nitrogendioxide_slant_column_density_precision.
    - Each variable is constructed in three dimensions: Time; Latitude; Longitude.

2. Ship track count data

    For the spatial validation, normarlized ship track count data is used. The original ship track count data is published by Halpern et al. Spatial and temporal changes in cumulative human impacts on the world’s ocean spatial validation, *Nature Communications* **2015**, *6*, 7615. [https://doi.org/10.1038/ncomms8615](https://doi.org/10.1038/ncomms8615)
    
3.
