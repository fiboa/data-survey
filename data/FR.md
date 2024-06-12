# France: Registre parcellaire graphique (RPG)

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Institut National de l'Information Géographique et Forestière (contact.geoservices@ign.fr )
- **Homepage:** https://www.data.gouv.fr/en/datasets/registre-parcellaire-graphique-rpg-contours-des-parcelles-et-ilots-culturaux-et-leur-groupe-de-cultures-majoritaire/

## Overview

France has published Crop Field data for many years. Crop fields are declared by farmers within the Common 
Agricultural Policy (CAP) subsidy scheme.

The anonymized version is distributed as part of the public service for making reference data available 
contains graphic data for plots (basic land unit for farmers' declaration) with their main crop. 
This data has been produced by the Services and Payment Agency (ASP) since 2007.

## Data

- **URL:** https://geoservices.ign.fr/rpg
- **Documentation:** https://geoservices.ign.fr/documentation/donnees/vecteur/rpg
- **File Format:** Shapefile, Geopackage
- **Projection:** EPSG:2154 (RGF93 / Lambert-93) for métropole (European France). Overseas territories (outre-mer) are published in suitable UTM- projections.
- **License:** "Licence Ouverte / Open Licence" https://etalab.gouv.fr/licence-ouverte-open-licence

License text at download page:
> _La réutilisation du RPG est gratuite pour tous les usages, y compris commerciaux, selon les termes de la "licence ouverte" version 2.0._

License text in [metadata](https://geoservices.ign.fr/sites/default/files/2023-11/IGNF_RPG_2-1.html): 
> _Base de données soumise aux conditions de la licence ouverte Etalab._

The mentioned [Etalab open License](https://etalab.gouv.fr/licence-ouverte-open-licence) is published 
by the government. There's an [English version](https://www.etalab.gouv.fr/wp-content/uploads/2018/11/open-licence.pdf)

### Properties

| Property   | Data Type | Constraints | Description               |
|------------|-----------|-------------|---------------------------|
| ID_PARCEL  | String    | 10 chars    | Identifier                |
| SURF_PARC  | Float     |             | Surface area              |
| CODE_CULTU | String    | 3 chars     | Main crop code            |
| CODE_GROUP | String    | 2 chars     | Group code of main crop   |
| CULTURE_D1 | String    | 3 chars     | Code of catch crop        |
| CULTURE_D1 | String    | 2 chars     | Code of second catch crop |

The textual descriptions of crop codes is referenced in the
[documentation](https://geoservices.ign.fr/documentation/donnees/vecteur/rpg). It's a CSV file called 
[Table référentielle des cultures et des groupes de cultures](https://geoservices.ign.fr/sites/default/files/2023-02/REF_CULTURES_GROUPES_CULTURES_2021.csv)

### Example

See an [example map at Géoportail](https://www.geoportail.gouv.fr/carte?c=4.067065654175731,49.19467447662851&z=15&l0=GEOGRAPHICALGRIDSYSTEMS.MAPS::GEOPORTAIL:OGC:WMTS(0.46)&l1=LANDUSE.AGRICULTURE2022::GEOPORTAIL:OGC:WMTS(1)&permalink=yes)

## API

| Standard | URL                                                                                               |
|----------|---------------------------------------------------------------------------------------------------|
| OGC WMTS | https://wxs.ign.fr/agriculture/geoportail/wmts?SERVICE=WMTS&VERSION=1.0.0&REQUEST=GetCapabilities |
| OGC WMS  | https://wxs.ign.fr/agriculture/geoportail/r/wms?SERVICE=WMS&VERSION=1.3.0&REQUEST=GetCapabilities |
| OGC WFS  | https://wxs.ign.fr/agriculture/geoportail/wfs?SERVICE=WFS&VERSION=2.0.0&REQUEST=GetCapabilities   |
