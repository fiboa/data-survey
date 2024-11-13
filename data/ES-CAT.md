# Catalonia Crop Fields (Mapa de cultius)

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Catalonia Department of Agriculture, Livestock, Fisheries and Food
- **Homepage:** https://agricultura.gencat.cat/ca/ambits/desenvolupament-rural/sigpac/mapa-cultius/

## Overview

The Department of Agriculture, Livestock, Fisheries and Food makes available to the public the data from the crop map of Catalonia.
This map allows you to locate the crops declared in the Agrarian Declaration - DUN submitted to the DACC.
The DUN is the tool for making the declarations of agricultural holdings in Catalonia. It is also used to apply for grants and to carry out certain procedures with the Department of Agriculture in an integrated manner. The geographical basis of declaration is the SIGPAC area. Owners of agricultural holdings that have productive agricultural surface (excluding those for own consumption) are required to declare annually.
Data from the DUN and the SIGPAC have been used to draw up this crop map. As the data declared are georeferenced, they can be located on the ground and this makes it possible to know, among other things, the identification of crops on each plot, the irrigation system and, depending on the cases, the second cultivation that is done in the plot
This information makes it possible to make an economic assessment of the impact that hailstorms have on crops, the effects of pests, fires, etc. and also lets you know the historical evolution of crops in the territory.

## Data

- **URL:** https://agricultura.gencat.cat/ca/ambits/desenvolupament-rural/sigpac/mapa-cultius/
- **Documentation:** https://agricultura.gencat.cat/web/.content/09-desenvolupament-rural/comu/dades_obertes/origen-dades-mapa-cultius.pdf
- **File Format:** GeoPackage / Shapefile
- **Projection:** EPSG:25831
- **License:** Open License, https://administraciodigital.gencat.cat/ca/dades/dades-obertes/informacio-practica/llicencies/

### Properties

| Property   | Data Type | Constraints | Description                                 |
|------------|-----------|-------------|---------------------------------------------|
| Campanya   | Integer   |             | campaign year                               |
| Provincia  | String    |             | Adminstrative subdivision Province          |
| Comarca    | String    |             | Adminstrative subdivision                   | 
| Municipi   | String    |             | Adminstrative subdivision municipality      |
| IDMUN      | String    |             | Municipality ID                             |                        
| Grup       | String    |             | Crop Group                                  |             
| Cultiu     | String    |             | Crop Name                                   |
| Seca_Regad | String    | S or R      | Irrigation coefficient (S=Dry, R=Irrigated) |                
| Sist_Regad | String    |             | Irrigation system used                      |              
| Varietat   | String    |             | Crop Variety                                |     
| Producte2n | String    |             | Second cultivated product                   |                
| HA         | Real      |             | Area                                        |


## API

| Standard  | URL                                                                            | Documentation   |
|-----------|--------------------------------------------------------------------------------|-----------------|
| OGC WMS   | http://sig.gencat.cat/ows/AGRICULTURA/wms                                      | -               |
| OGC WFS   | https://sig.gencat.cat/ows/AGRICULTURA/wfs?request=getcapabilities&service=wfs | -               |

### Example

https://sig.gencat.cat/visors/Cultius_DUN_SIGPAC.html
https://analisi.transparenciacatalunya.cat/Medi-Rural-Pesca/Mapa-de-cultius-de-Catalunya-amb-origen-DUN/e7kw-9ebb
