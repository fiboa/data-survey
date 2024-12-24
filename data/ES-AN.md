# Andalucia SIGPAC

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Junta de Andalucia - La consejería de Agricultura, Pesca, Agua y Desarollo Rural
- **Homepage:** https://www.juntadeandalucia.es/organismos/agriculturapescaaguaydesarrollorural.html

## Overview

SIGPAC is the Geographic Information System for the Identification of Agricultural Plots , 
created through collaboration between the Spanish Agricultural Guarantee Fund (FEGA) and 
the different Autonomous Communities, within the scope of their territories, as an element 
of the Integrated Management and Control System of the direct aid regimes. It has the character 
of a public register of administrative profile, and contains updated information on the 
plots that may benefit from community aid related to the surface area, providing graphic 
support for these and their subdivisions (ENCLOSURES) with defined agricultural uses or 
developments.

## Data

- **URL:** https://www.juntadeandalucia.es/organismos/agriculturapescaaguaydesarrollorural/servicios/sigpac/visor/paginas/sigpac-descarga-informacion-geografica-shapes-provincias.html
- **Documentation:** https://www.juntadeandalucia.es/sites/default/files/inline-files/2024/03/Metadatos_Recintos_Sigpac_2024.pdf
- **File Format:** Shapefile
- **Projection:** EPSG:4258
- **License:** CC-SA-BY-ND / Pursuant to Law 37/2007 of 16 November on the reuse of public sector information and Law 3/2013 of 24 July approving the Statistical and Cartographic Plan of Andalusia 2013-2017, the geographic information of SIGPAC is made available to the public.
- **License:** https://www.juntadeandalucia.es/organismos/agriculturapescaaguaydesarrollorural/servicios/sigpac/visor/paginas/sigpac-descarga-informacion-geografica-shapes-provincias.html#toc-condiciones-de-uso-para-la-licencia-de-uso-comercial
- **Attribution:** ©Junta de Andalucía

### Properties

| Property   | Data Type | Constraints | Description          |
|------------|-----------|-------------|----------------------|
| ID_RECINTO | Real      |             | Identifier           |
| CD_PROV    | Integer   |             | Province code        |
| CD_MUN     | Integer   |             | Municipality code    |
| CD_AGRE    | Integer   |             |                      |
| CD_ZONA    | Integer   |             |                      |
| CD_POL     | Integer   |             |                      |
| CD_PARCELA | Integer   |             |                      |
| CD_RECINTO | Integer   |             |                      |
| CD_USO     | String    |             | Land Use Code (Crop) |
| NU_AREA    | Real      |             | Used area            |
| CSP        | Integer   |             |                      |
| COEF_REG   | Integer   |             |                      |
| PDTE_MEDIA | Real      |             |                      |
| INCIDENCIA | String    |             |                      |
| REGION     | Integer   |             |                      |
| GC         | String    |             |                      |
| VER        | String    |             |                      |


## Example

http://ws128.juntadeandalucia.es/agriculturaypesca/sigpac/index.xhtml