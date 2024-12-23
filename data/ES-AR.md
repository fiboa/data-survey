# Aragon SIGPAC

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Gobierno de Aragorn
- **Homepage:** https://www.aragon.es/

https://idearagon.aragon.es/descargas

## Overview

SIGPAC - Sistema de Información Geográfica de la Política Agrícola común (ejercicio actual)

Geographic Information System (SIGPAC) updated and coordinated with the land registry that allows 
the geographical identification of plots declared by farmers in any aid scheme related to the surface area.
Published by the Aragon local government.

## Data

- **URL:** https://icearagon.aragon.es/descargas?coleccion=SIGPAC
- **File Format:** Shapefile
- **Projection:** EPSG:25830
- **License:** CC-BY-4.0 see https://idearagon.aragon.es/portal/politica-privacidad.jsp
- **Attribution:** (c) Gobierno de Aragon

### Properties

| Property   | Data Type | Constraints | Description       |
|------------|-----------|-------------|-------------------|
| DN_OID     | Real      |             | Identifier        | 
| SUPERF.    | Real      |             | Area in m^2       | 
| PROVINCIA  | Integer   |             | Province code     | 
| MUNICIPIO  | Integer   |             | Municipality code | 
| AGREGADO   | Integer   |             |                   |
| ZONA       | Integer   |             |                   |
| POLIGONO   | Integer   |             |                   | 
| PARCELA    | Integer64 |             |                   |
| RECINTO    | Integer64 |             |                   |
| ELEGIBILID | Integer   |             |                   |
| PENDIENTE_ | Integer   |             |                   |
| COEF_REGAD | Integer   |             |                   |
| COEF_ADMIS | Integer   |             |                   |
| USO_SIGPAC | String    |             | Crop code         |
| PARCELA_AG | String    |             |                   |
| GRUPO_CULT | String    |             | Crop Group        |
| REGION     | Integer   |             |                   |

## API

See https://icearagon.aragon.es/portal/directorio_ws.jsp for Aragon APIs

## Examplea

https://icearagon.aragon.es/cartoteca/index.html?LOCAT=http://idearagon.aragon.es/Visor2D?&SERVICIO=Visor2D&CAPA=v_sigpac_recintos&BBOXFOTOGRAMA=649005.99350000:4581760.39700000:810495.30640000:4754860.70140000&ESCALA=5000&COLECCION=SIGPAC&ISGEORREF=false&FECHA=20240101
