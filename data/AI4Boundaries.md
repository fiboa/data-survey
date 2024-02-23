# AI4Boundaries

## Submission Details

- **Submitter (Affiliation):** Matej Batič
- **Data Provider (Legal Entity):** European Commission, Joint Research Centre
- **Homepage:** https://data.jrc.ec.europa.eu/dataset/0e79ce5d-e4c8-4721-8773-59a4acf2c9c9

## Overview

AI4Boundaries is a data set of images and labels readily usable to train and compare models on field boundary detection. AI4Boundaries includes two specific data sets: 
  (i) a 10 m Sentinel-2 monthly composites for large-scale analyses in retrospect and 
  (ii) a 1 m orthophoto data set for regional-scale analyses, such as the automatic extraction of Geospatial Aid Application (GSAA). 

All labels have been sourced from GSAA data that have been made openly available (Austria, Catalonia, France, Luxembourg, the Netherlands, Slovenia, and Sweden) for 2019, representing 14.8 M parcels covering 376 K km2. Data were selected following a stratified random sampling drawn based on two landscape fragmentation metrics, the perimeter/area ratio and the area covered by parcels, thus considering the diversity of the agricultural landscapes. The resulting AI4Boundaries dataset consists of 7831 samples of 256 by 256 pixels for the 10 m Sentinel-2 dataset and of 512 by 512 pixels for the 1 m aerial orthophoto. Both datasets are provided with the corresponding vector ground-truth parcel delineation (2.5 M parcels covering 47 105 km2), and with a raster version already pre-processed and ready to use.

More about the dataset, together with a discussion on the perspectives and limitations of the dataset for various types of applications in the agriculture domain and considerations of possible further improvements is available in the paper _AI4Boundaries: an open AI-ready dataset to map field boundaries with Sentinel-2 and aerial photography_, Earth Syst. Sci. Data, 15, 317–329, https://doi.org/10.5194/essd-15-317-2023, 2023.


## Data & Metadata

- **URL:** https://jeodpp.jrc.ec.europa.eu/ftp/jrc-opendata/DRLL/AI4BOUNDARIES/  
- **Documentation:** d'Andrimont, R., Claverie, M., Kempeneers, P., Muraro, D., Yordanov, M., Peressutti, D., Batič, M., and Waldner, F.: _AI4Boundaries: an open AI-ready dataset to map field boundaries with Sentinel-2 and aerial photography_, Earth Syst. Sci. Data, 15, 317–329, https://doi.org/10.5194/essd-15-317-2023, 2023.
- **File Format:** GeoPackage for vectors, TIFF (for imagery and masks)
- **Projection:** EPSG:3035
- **License:** Creative Commons Attribution 4.0 International (CC BY 4.0) licence

A python-based library is also available to facilitate download of the dataset: https://github.com/waldnerf/ai4boundaries

### Properties

[ai4boundaries_sampling.gpkg](https://jeodpp.jrc.ec.europa.eu/ftp/jrc-opendata/DRLL/AI4BOUNDARIES/sampling/ai4boundaries_parcels_vector_sampled.gpkg) is a GeoPackage vector file containing the 7831 4-by-4 km polygons of the sampled fields along with the sampling stratification values as attributes.

| Property    | **Data Type** | Description |
| ----------- | ------------- | ----------- |
| id          | number        | grid cell identifier  |
| par         | number        | parcel perimeter/area ratio |
| farea       | number        | ? |
| parea       | number        | ? |
| fperimeter  | number        | ? |
| cnt         | number        | Number of features (parcels) in grid cell |
| av_perimet  | number        | Average of perimeter (grid_sel.perimeter / grid_sel.cnt) |
| adm         | string        | Administrative area |
| par_c       | number        | reclassified parcel perimeter/area ratio |
| area_c      | number        | reclassified area |
| gid         | number        | ? |
| id_2        | number        | parcel unique identifier |
| coutry      | string        | should be equal to administrative area |
| year        | number        | year of parcel data |

