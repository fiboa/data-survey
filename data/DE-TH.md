# Thuringia (TH), Germany

## Submission Details

- **Submitter (Affiliation):** Matthias Mohr
- **Data Provider (Legal Entity):** Land Thüringen (Government)
  - Contact: Thüringer Landesamt für Landwirtschaft und Ländlichen Raum 

- **Homepage:** https://geomis.geoportal-th.de/geonetwork/srv/ger/catalog.search#/metadata/D872F2D6-60BC-11D6-B67D-00E0290F5BA0

## Overview

Field boundaries for Thuringia (German: Thüringen).

For use in the application procedure of the Integrated Administration and Control System (IACS), digital data layers are required that represent the current situation of agricultural use with the required accuracy. The field block is a contiguous agricultural area of one or more farmers surrounded by permanent boundaries. The field block thus contains information on the geographical location of the outer boundaries of the agricultural area. Reference parcels are uniquely numbered throughout Germany (Feldblockident - FBI). They also have a field block size (maximum eligible area) and a land use category. 

The following field block types exist:

- Utilized agricultural area (UAA)
- Landscape elements (LE)
- Special use areas (SF)
- Forest areas (FF)

The field blocks are classified separately according to the main land uses of arable land (`AL`), grassland (`GL`), permanent crops (`DA`, `OB`, `WB`), including agroforestry systems with an approved utilization concept and according to the BNK for no "agricultural land" (`NW`, `EF` and `PK`) and others. 

Landscape elements (LE) are considered part of the eligible agricultural area under defined conditions. In Thuringia, these permanent conditional features are designated as a separate field block (FB) and are therefore part of the Thuringian area reference system (field block reference). They must have a clear reference to an UAA (agricultural land), i.e. they are located within an arable, permanent grassland or permanent crop area or border directly on it. 

To produce the DGK-Lw, (official) orthophotos from the Thuringian Land Registry and Surveying Administration (TLBG) and orthophotos from the TLLLR's own aerial surveys are interpreted. The origin of this image data is 50% of the state area each year, so that up-to-date image data is available for the entire Thuringian state area every year.

## Data & Metadata

- **URL:**
  - DGK: https://www.geoproxy.geoportal-th.de/download-service/opendata/agrar/DGK_Thue.zip
  - DFK: https://www.geoproxy.geoportal-th.de/download-service/opendata/agrar/DFK_Thue.zip
- **Documentation:** included in the ZIP files above
- **File Format:** Shapefile
- **Geometry Format (if different from data):** -
- **Metadata Format (if different from data):** INSPIRE
- **Projection:** EPSG:25832 (ETRS89 / UTM Zone 32N)
- **License:** [Data licence Germany – attribution – Version 2.0](https://www.govdata.de/dl-de/by-2-0)
- **Attribution:** © GDI-Th

### Properties

#### DGK

| Property   | Data Type | Constraints | Description |
| ---------- | --------- | ----------- | ----------- |
| BEZUGSJAHR | string    | 4 chars     | Year, for which the data is valid                            |
| FBI        | string    | 16 chars    | FLIK Identifier, e.g. `DETHLIGL46281S17`                     |
| FBI_KURZ   | string    | 10 chars    | FLIK id without country, state and type prefix (`DETHLI`), e.g. `GL46281S17` |
| FB_FLAECHE | double    | 17;4 digits | Area, in ha                                                  |
| FBI_VJ     | string    | 254 chars   | FLIK identifier(s) of the previous year, separated by comma and space |
| FB_FL_VJ   | double    | 17;4 digits | Area in the previous year, in ha                             |
| TK10       | string    | 5 chars     | Paper of the 1:10,000 topographic map in which the center of where the center of gravity of the field block lies. Example: `51334` |
| AFO | string | 1 char | Agroforestry system |
| LF | string | 2 chars | Field block type, see below. |
| BNK | string | 2 chars | Category of land use, short code, see below. |
| KOND_LE | string | 1 char | All permanent LE landscape elements in Thuringia are conditionalities-LE and are recorded as a field block. One of:`J` or null |
| AENDERUNG | string | 80 chars | Whether the field was updates since the last update - One of:  `Unveraendert` – `Geaendert` – `Neu` |
| GEO_UPDAT | string | 10 chars | Date of last geometry update |

Values for `LF`:

- `LF` Agriculturally usable area
- `LE` Landscape element
- `SF` Special use area
- `FF` Forestry area

Values for `BNK`:

- `AF` Agroforestry strips on arable land
- `AL` Arable land
- `BR` Row of trees
- `DK` Permanent crops (includes the BNK DA, OB and WB valid in TH until 2023)
- `EB` Single tree (as natural monument)
- `EF` First afforestation (DZ-eligible)
- `FG` Wetland and pond
- `FH` Field copse
- `FO` Forest field block (forest, not from first afforestation)
- `FR` Field margin
- `FS` Rock and stone bar
- `GL` Grassland
- `HK` Hedge
- `NT` Stone walls, dry stone and natural stone walls
- `NW` Nature and water conservation (DZ-eligible)
- `OL` Open land conservation (KULAP-eligible)
- `TR` Terrace
- `WA` Forest from first afforestation (not DZ-eligible)

#### DFK

omitted for now, see documentation in the ZIP files

## API

| Standard | URL | Documentation |
| -------- | --- | ------------- |
| OGC WMS  | https://www.geoproxy.geoportal-th.de/geoproxy/services | - |
