# Spain Canary Islands Crop fields

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Gobierno de Canarias - Consejería de Agricultura, Ganadería, Pesca y Soberanía Alimentaria
- **Homepage:** https://www.gobiernodecanarias.org/agpsa/

## Overview

The Canary Islands Crop Map is a cartographic dataset developed by the Department of Agriculture, Livestock,
Fisheries and Water of the Government of the Canary Islands, to understand the reality of the available
agricultural surface of the Canary Islands. This tool has been developed from 1998 to the present.

There are several crop maps for each of the islands, which allow us to see the temporal and spatial evolution
of the cultivated areas of the islands in recent years. All this means that the Canary Islands Crop Map is a
basic tool for decision-making in present and future regional agricultural policy, as well as being a basic
source for the preservation of agricultural land in the field of territorial planning.

The data of the Canary Islands Crop Map have been published on the 
[open data portal of the Government of the Canary Islands](https://datos.canarias.es/catalogos/general/dataset/mapa-de-cultivos-de-canarias)
and in [datos gob](https://datos.gob.es/es/catalogo/a05003638-mapa-de-cultivos-de-canarias1), 
this work having been addressed within the Strategic Plan for Innovation and Continuous Improvement 
of the Ministry of Agriculture, Livestock and Fisheries.

The actions carried out have been developed in the following phases:
1. Compilation of the different sources referring to crops in the Canary Islands from the Ministry of Agriculture, Livestock and Fisheries.
2. Analysis of the existing standards at European, national and regional level.
3. Creation of the necessary classifications for the standardisation of the crop map.
4. Proposal of a unique coding of crops for the dissemination of data.
5. Adaptation of the current data to the proposed coding.
As a result of this work, it has been possible to standardise the data referring to crops in the Canary Islands, adjusting the publication to international standards, eliminating confusing codings, avoiding duplications and simplifying data collection.

## Data

- **URL:** https://datos.canarias.es/catalogos/general/dataset/mapa-de-cultivos-de-canarias
- **URL:** https://www.gobiernodecanarias.org/agricultura/temas/mapa_cultivos
- **Alternative:** https://opendata.sitcan.es/dataset/mapa-de-cultivos-de-canarias
- **Documentation:** https://opendata.sitcan.es/upload/medio-rural/gobcan_mapa-cultivos_metodologia.pdf
- **Legal Framework:** https://www.gobiernodecanarias.org/boc/2023/090/010.html
- **File Format:** Shapefile+Zip, one per island
- **Projection:** EPSG:32628
- **License:** CC-BY-4.0
- **Attribution:** Gobierno de Canarias

### Properties

| Property   | Data Type | Constraints | Description   |
|------------|-----------|-------------|---------------|
| ISLA_NA    | String    |             | Island name   |
| ISLA_CO    | String    |             | Island code   |
| CULTIVO_NA | String    |             | Crop name     |
| CULTIVO_CO | String    |             | Crop code     |
| BORDE_NA   | String    |             |               |
| BORDE_CO   | String    |             |               |
| DISEMI_NA  | String    |             |               |
| DISEMI_CO  | String    |             |               |
| REGADIO_NA | String    |             |               |
| REGADIO_CO | Integer   |             |               |
| TECNICA_NA | String    |             |               |
| TECNICA_CO | String    |             |               |
| ABANDON_NA | String    |             |               |
| ABANDON_CO | String    |             |               |
| AREA_M2    | Real      |             | Area in m2    |
| FECHA      | String    |             | Date of field |
