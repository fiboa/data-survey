# Geneva, Switzerland

## Submission Details

- **Submitter (Affiliation):** Saidy Barry, moreGeo GmbH
- **Data Provider (Legal Entity):** État de Genève, Office cantonal de l'agriculture et de la nature, distributed by SITG (Government)
- **Homepage:** https://ge.ch/sitg/

## Overview

The agricultural parcels that Geneva's farmers georeference every year for the direct payments ("surfaces
agricoles recensées"). SITG publishes every year since 2017 in one layer, split by `EXERCICE`, and rebuilds the
downloads weekly. The current year is provisional until December. The usage code is the federal one, the names
are French. The canton's file on [geodienste.ch](CH.md) is the same register.

## Data

- **URL:** https://ge.ch/sitg/geodata/SITG/OPENDATA/AGR_SURFACE_AGRICOLE_RECENSEE-SHP.zip (also `-GDB`, `-GML`, `-CSV`); ArcGIS REST https://vector.sitg.ge.ch/arcgis/rest/services/AGR_SURFACE_AGRICOLE_RECENSEE/FeatureServer/0
- **Documentation:** metadata PDF inside the zip (`DOC/AGR_SURFACE_AGRICOLE_RECENSEE.pdf`)
- **File Format:** Shapefile, File Geodatabase, GML, CSV (zipped); ArcGIS REST; WFS
- **Projection:** EPSG:2056 (CH1903+ / LV95)
- **License:** [SITG conditions d'utilisation, level A "Accès libre"](https://sitg.ge.ch/ressources/conditions-utilisation-donnees): private and commercial use, the source must be cited
- **Attribution:** "Données SITG", with the date of extraction

Rows per year: 9,519 (2017), 9,695 (2018), 9,619 (2019), 9,732 (2020), 9,716 (2021), 9,810 (2022), 9,992 (2023),
10,101 (2024), 10,014 (2025), 10,204 (2026, provisional). `SHAPE_AREA` is the geometry area in m². 45 rows have
no code; the codes 891 and 929 are Geneva's own and not in the federal catalogue.

### Properties

| Property   | Data Type | Constraints     | Description                                  |
|------------|-----------|-----------------|----------------------------------------------|
| ID         | string    | `GE_<year>_<n>` | Identifier                                   |
| CODE_FED   | integer   |                 | Federal usage code (LNF), e.g. `513`         |
| TYPE       | string    | French          | Usage name, e.g. `Blé d'automne`             |
| THEMATIQUE | string    |                 | Use group, e.g. `Grandes cultures`           |
| SAU        | string    | oui/non         | Within the utilised agricultural area        |
| SPB        | string    | oui/non         | Biodiversity promotion area                  |
| EXERCICE   | integer   | 2017–2026       | Year of the census                           |
| SHAPE_AREA | number    | m²              | Area                                         |
