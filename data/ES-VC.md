# Agricultural Plots in the Valencian Community (SIGPAC)

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Spanish Agricultural Guarantee Fund (FEGA) of the Ministry of Agriculture, Fisheries and Food
- **Homepage:** https://www.fega.gob.es/es/PwfGcp/es/el_fega/index.jsp
- 
## Overview

Graphic layer of the plots and enclosures with defined agricultural uses that accompany the information of the 
Geographic Information System (SIGPAC) in the Valencian Community valid for the SIGPAC 2024 campaign 
(data dated 15-01-2024). The SIGPAC is the Geographic Information System for the Identification of Agricultural Plots 
dedicated to the control of agricultural aid of the Common Agricultural Policy (CAP), which arises through the 
collaboration between the Spanish Agricultural Guarantee Fund (FEGA) and the Agriculture Councils of the CCAA. 
It is a public registry of administrative profile that contains updated information on the plots likely to benefit from 
community aid related to the surface area.

## Data

- **URL:** https://dadesobertes.gva.es/dataset/sistema-de-informacion-geografica-de-parcelas-agricolas-de-la-comunitat-valenciana-sigpac-2024
- **Documentation**: https://catalogo.icv.gva.es/geonetwork/srv/spa/catalog.search#/metadata/spaicv1403_sigpac2024
- **File Format:** Shapefile, OGC Web services
- **Projection:** EPSG:25830  /EPSG:3042
- **License:** CC-BY-4.0 (taken from http://www.icv.gva.es/condiciones-de-uso-de-la-geoinformacion-icv )
- **Attribution:** 1403_2024PAC0050 CC BY 4.0 © Institut Cartogràfic Valencià, Generalitat

### Properties

| Property   | Data Type | Constraints | Description     |
|------------|-----------|-------------|-----------------|
| DN_OID     | Integer   |             |                 |
| DN_SURFACE | Real      |             | Area in m^2     |
| DN_PERIMET | Real      |             | Perimeter in m  |
| PROVINCIA  | Integer   |             | Province ID     |
| MUNICIPIO  | Integer   |             | Municipality ID |
| AGREGADO   | Integer   |             |                 |
| ZONA       | Integer   |             |                 |
| POLIGONO   | Integer64 |             |                 |
| PARCELA    | Integer64 |             |                 |
| RECINTO    | Integer64 |             |                 |
| PENDIENTE_ | Integer64 |             |                 |
| ALTITUD    | Integer64 |             |                 |
| COEF_REGAD | String    |             |                 |
| USO_SIGPAC | String    |             | SIGPAC use code |
| INCIDENCIA | String    |             |                 | 
| PARCELA_AG | String    |             |                 | 
| GRUPO_CULT | String    |             |                 | 
| REGION     | Integer64 |             |                 |
| ALMENDROS  | Integer64 |             |                 |
| ALGARROBOS | Integer64 |             |                 |
| NOGALES    | Integer64 |             |                 |
| PISTACHOS  | Integer64 |             |                 |
| OTROS      | Integer64 |             |                 |
| CASTANOS   | Integer64 |             |                 |
| X_ETRS8930 | Real      |             |                 | 
| Y_ETRS8930 | Real      |             |                 |
| X_ED5030   | Real      |             |                 | 
| Y_ED5030   | Real      |             |                 |
| CAP_PREV   | Real      |             |                 |

Webviewer: https://visor.gva.es/visor/?capas=spaicv1403_sigpac2024

## API

| Standard | URL                                                                           |
|----------|-------------------------------------------------------------------------------| 
| OGC WMS  | https://terramapas.icv.gva.es/1403_SIGPAC?service=WMS&request=GetCapabilities |
| OGC WFS  | https://terramapas.icv.gva.es/1403_SIGPAC?service=wfs&request=getcapabilities |
