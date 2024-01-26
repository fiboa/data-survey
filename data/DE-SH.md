# Schleswig-Holstein (SH), Germany

## Submission Details

- **Submitter (Affiliation):** Matthias Mohr
- **Data Provider (Legal Entity):** Land Schleswig-Holstein (Government)
- **Homepage:** https://sh-mis.gdi-sh.de/catalog/?lang=de#/datasets/iso/21f67269-780f-4f3c-8f66-03dde27acfe7

## Overview

Field blocks in Schleswig-Holstein.

## Data

- **URL:**
  - GeoPackage: https://service.gdi-sh.de/SH_OpenGBD/feeds/Atom_SH_Feldblockfinder_OpenGBD/data/Feldbloecke_2024_GPKG.zip
  - Shapefile: https://service.gdi-sh.de/SH_OpenGBD/feeds/Atom_SH_Feldblockfinder_OpenGBD/data/Feldbloecke_2024_SHP.zip
- **Documentation:** no direct link. visit homepage, click "PDF herunterladen"
- **File Format:** Shapefile / GeoPackage
- **Geometry Format (if different from data):** -
- **Projection:** EPSG:25832 (UTM 32N) or EPSG:4258 (ETRS89)
- **License:** [Deutschland – Zero – Version 2.0](https://www.govdata.de/dl-de/zero-2-0)

## Metadata

- **Documentation:** -
- **Metadata Format (if different from data):** INSPIRE

| Property   | Data Type | Constraints | Description |
| ---------- | --------- | ----------- | ----------- |
| fid        | integer   |             | Identifier. Example. `123` |
| fachguelti | string    | Date        | Valid for; Usually describes the year. Example: `01.01.2024` |
| FLIK       | string    | 50 chars    | Area identifier for field blocks. Example: `DESHLIL020110002` |
| Flaeche    | number    |             | Area in ha |
| HBN        | string    | 50 chars    | Category of main land use (see below) |
| SHAPE_AREA | number    | > 0         | Shapefile only: Area of the shape in m² |
| SHAPE_LEN  | number    | > 0         | Shapefile only: Length of the shape (i.e. boundary) in meters |

Values for `HBN`:
- `Ackerland` (arable land)
- `Dauerkultur` (permanent crops)
- `Dauergrünland` (permanent grassland)
- `Nicht landwirtschaftliche förderfähige Flächen` (Areas not eligible for agricultural subsidies)
- `Sonstige nicht ldw. genutzte Flächen` (Other non-agricultural land)

## API

| Standard | URL | Documentation |
| -------- | --- | ------------- |
| ATOM     | https://sh-mis.gdi-sh.de/catalog/?lang=de#/datasets/iso/cc68aa82-d71b-42bb-b5ce-7b850486a842 | https://sh-mis.gdi-sh.de/catalog/?lang=de#/datasets/iso/cc68aa82-d71b-42bb-b5ce-7b850486a842 |
| OGC WMS  | 	https://service.gdi-sh.de/WMS_SH_Feldblockfinder?SERVICE=WMS&VERSION=1.3.0&REQUEST=GetMap&LAYERS=Feldblöcke | - |
