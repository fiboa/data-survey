# Navarra SIGPAC

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Foral Community of Navarre  (Comunidad Foral de Navarra)
- **Homepage:** https://www.fega.gob.es/orig/

## Overview

Geographic Information System (SIGPAC) updated and coordinated with the land registry that allows 
the geographical identification of plots declared by farmers in any aid scheme related to the surface area.

Link to download SIGPAC graphic and alphanumeric information by municipality: 
graphic in ESRI Shape format (in ETRS89 UTM 30N reference system) and alphanumeric in CSV format.

## Data

- **URL:** https://filescartografia.navarra.es/2_CARTOGRAFIA_TEMATICA/2_6_SIGPAC/
- **Documentation:** https://sigpac.navarra.es/descargas/
- **Documentation:** https://datos.gob.es/es/catalogo/a15002917-sigpac-recintos-sigpac
- **File Format:** Shapefile+ZIP (per municipality)
- **Projection:** EPSG:25830
- **License:** CC-BY-4.0
- **Attribution:** Comunidad Foral de Navarra

### Properties

| Property   | Data Type | Constraints    | Description       |
|------------|-----------|----------------|-------------------|
| FEATURE    | Integer64 |                | ID                |
| REFSIGPAC  | String    | max_length=25  | SIGPAC ID         |
| CP         | Integer64 |                |                   |
| CMUNICIPIO | Integer64 |                | Municipality code |
| MUNICIPIO  | String    | max_length=100 | Municipality name |
| POLIGONO   | Integer64 |                |                   |
| PARCELA    | Integer64 |                |                   |
| CRECINTO   | Integer64 |                |                   |
| IDUSO24    | String    | max_length=25  | USE_CODE          |
| USO24      | String    | max_length=100 | USE_CODE_NAME     |
| INCIDENCIA | String    | max_length=50  |                   |
| IDUSO03    | String    | max_length=100 |                   |
| TIPOEXPLOT | String    | max_length=50  |                   |
| CSUBVENCI  | String    | max_length=5   |                   |
| PENDIENTE  | Integer64 |                |                   |
| IDCOMARCA  | String    | max_length=25  | Comarca ID        |
| COMARCA    | String    | max_length=100 | Comarca name      |
| REGION     | String    | max_length=5   | Region ID         |
| BEGINLIFE  | String    | max_length=10  | Date DD/MM/YYYY   |
| SUPERFICIE | Real      |                |                   |
