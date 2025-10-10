# Brazilia CONAB fields

## Submission Details

- **Submitter (Affiliation):** Tristan Grupp / Ivor Bosloper
- **Data Provider (Legal Entity):** CONAB, Brazil's Government agency responsible for providing information on the country's agricultural harvest
- **Homepage:** https://portaldeinformacoes.conab.gov.br/

## Overview

Approximately 80k boundaries. After inspecting all boundaries in the CONAB public database, appear to be hand-drawn field boundaries.

Some boundaries might encapsulate multiple fields so could be split by road line geometries to improve them.

Otherwise, filter them out by size OR potentially filter with randomly sampled points within each polygons, extracting NDVI time series to each point, filtering out boundaries whose points are too different in their time series of NDVI.

## Data

- **URL:** https://portaldeinformacoes.conab.gov.br/mapeamentos-agricolas-downloads.html
- **Documentation:** https://docs.data.example
- **File Format:** Shapefile+ZIP
- **Projection:** EPSG:4674
- **License:** CC-BY-NC

License definition derived from:

> O conteúdo dos Mapeamentos tem como fonte a Conab, a reprodução total ou parcial sem fins lucrativos é autorizada, desde que citada a fonte e mantendo a integridade das informações.

> The content of the Mappings comes from Conab, total or partial reproduction without profit is authorized, as long as the source is cited and the integrity of the information is maintained.

### Properties

This is the combined mix of properties of the different shapefiles

| Property   | Data Type | Constraints | Description                                |
|------------|-----------|------------|--------------------------------------------|
| id         | number    |            | Not so usefull combining multiple datasets |
| cd_mun     | number    |            | Municipality code                          |
| nm_mun     | string    |            | Municipality name                          |
| area_ha    | number    |            | Area in ha                                 |
| CD_MUN     | number    |            | Municipality code                          |
| NM_MUN     | string    |            | Municipality name                          |
| SIGLA_UF   | number    |            |                                            |
| CD_GEOCMU  | number    |            |                                            |
| OBJECTID_1 | number    |            |                                            |
| DS_USO     | number    |            |                                            |
| CD_UGT     | string    |            |                                            |
| CD_IBGE_MU | number    |            |                                            |
| NM_MUNIC   | string    |            |                                            |
| NM_MICRO_R | string    |            | Municipality name ?                        |
| Shape_Leng | number    |            | Perimeter                                  |
| Shape_Area | number    |            | Area in ..                                 |
| Hectares   | number    |            | Area in ha                                 |
| REGIAO     | string    |            |                                            |
| sigla_uf   | string    |            |                                            |
