# Spain Castile and León Crop fields (SIGPAC)

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Spain Castilla y León
- **Homepage:** https://www.itacyl.es/

## Overview

Official SIGPAC land plan for the year 2024 (reference date 02-01-2024)
Data is based on the SIGPAC (FEGA) database.

The content of each *.zip file is 3 files in SHP format with their respective auxiliaries, each of them represents:

1. The polygons called (POLFE.* )  
2. The plots called (PARFE.* )
3. The enclosures called (RECFE.* )

Free use of the data is permitted, but commercial exploitation is prohibited.

## Data

- **URL:** http://ftp.itacyl.es/cartografia/05_SIGPAC/
- **Documentation:** http://ftp.itacyl.es/cartografia/05_SIGPAC/Catalogo_Metadatos/
- **File Format:** Shapefile+ZIP, spread over 255 zip-files
- **Projection:** EPSG:4258
- **License:** CC-NC (a Non-free license)
- **Attribution:** Not for non-commercial use

### Properties

| Property   | Data Type | Constraints | Description     |
|------------|-----------|-------------|-----------------|
| DN_OID     | Integer64 |             |                 |
| SUPERFICIE | Real      |             | Area in m^2     |
| PERIMETRO  | Real      |             | Perimeter in m  |
| PROVINCIA  | Integer64 |             | Province ID     |
| MUNICIPIO  | Integer64 |             | Municipality ID |
| AGREGADO   | Integer64 |             |                 |
| ZONA       | Integer64 |             |                 |
| POLIGONO   | Integer64 |             |                 |
| PARCELA    | Integer64 |             |                 |
| RECINTO    | Integer64 |             |                 |
| USO_SIGPAC | String    |             | SIGPAC use code |
| COEF_REGAD | Integer64 |             |                 |
| C_REFREC   | String    |             |                 |
| Shape_Leng | Real      |             |                 |
| Shape_Area | Real      |             |                 |

