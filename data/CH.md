# Switzerland

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper; cantons by Saidy Barry, moreGeo GmbH
- **Data Provider (Legal Entity):** The 26 cantons (Government), distributed by the Konferenz der kantonalen Geoinformations- und Katasterstellen (KGK-CGC) on geodienste.ch
- **Homepage:** https://www.geodienste.ch/services/lwb_nutzungsflaechen

## Overview

The agricultural usage areas of Switzerland ("Nutzungsflächen", federal model 153.1) are the plots whose use each
canton records as the basis for direct payments. Every canton publishes its own data under its own terms;
geodienste.ch distributes them as one GeoPackage per canton in the shared model, current state only. Three cantons
keep earlier years on their own portals: [Zürich](CH-ZH.md) (2017–2025), [Geneva](CH-GE.md) (2017–2026) and
[Schwyz](CH-SZ.md) (2022–2024).

## Data

- **URL:** One GeoPackage per canton, the `geopackage_zip` asset of the STAC items at https://www.geodienste.ch/stac/collections/lwb_nutzungsflaechen/items ; availability and terms per canton in https://www.geodienste.ch/info/services.json?base_topics=lwb_nutzungsflaechen
- **Documentation:** https://www.geodienste.ch/services/lwb_nutzungsflaechen and https://geobasisdaten.ch/detail/818418/ ; usage codes: https://fiboa.org/code/ch/lnf_code.csv
- **File Format:** GeoPackage (also INTERLIS, Shapefile, WFS)
- **Projection:** EPSG:2056 (CH1903+ / LV95)
- **License:** Per canton (table below): the [opendata.swiss terms of use](https://opendata.swiss/en/terms-of-use), which are terms of use rather than licences, plus the canton's own conditions. "Source required" asks for author, title and link to the dataset.

BS ships an empty file, its plots are in the BL file. AG, AR, NW, OW, SG, UR and ZH publish on model version 2.0,
the others on 3.0, with the same columns. The `ist_ueberlagernd` flag marks overlapping landscape elements that
would otherwise duplicate the area. Cantons that require registration or approval are converted from an exported
file: `fiboa convert ch_<canton> -i <zip>|geopackage/*.gpkg`.

### Terms of use per canton

From the Info column of each canton on the service page (2026-09-24); prescribed source wording in quotes.

| Canton | Availability | opendata.swiss term | Cantonal conditions | Own archive |
| --- | --- | --- | --- | --- |
| AG | free | Open use, source required | [ag.ch](https://www.ag.ch/geoportal/geodatenshop/Nutzungsbedingungen.aspx?Typ=NutzungsbedingungenAGIS1), "Daten des Kantons Aargau" | – |
| AI | free | Open use, source required | [PDF](https://www.geodienste.ch/pdfs/AI/lwb_nutzungsflaechen/data/Nutzungsbedingungen_AI_annex-123-2.pdf), "Grundlage/Quelle: Geodaten Kanton/Bezirke Appenzell I.Rh." | – |
| AR | free | Open use | [PDF](https://ar.ch/fileadmin/user_upload/Departement_Bau_Volkswirtschaft/Amt_fuer_Raum_Wald/Geoinformation_und_Vermessung/AR_Nutzungsbedingungen_Geodaten.pdf) | – |
| BE | free | Open use, source required | [agi.dij.be.ch](https://www.agi.dij.be.ch/de/start/geoportal/geodaten/detail.html?type=geoproduct&code=LANDKULT) | – |
| BL | free | Open use, source required | [baselland.ch](https://www.baselland.ch/politik-und-behorden/direktionen/volkswirtschafts-und-gesundheitsdirektion/amt-fur-geoinformation/geoportal/geodaten/nutzung-von-geodaten) | – |
| BS | free, empty file | Open use, source required | [bs.ch](https://www.bs.ch/bvd/grundbuch-und-vermessungsamt/geo/anwendungen/agb) (CC BY 4.0), "Quelle: Geodaten Kanton Basel-Stadt" | – |
| FR | free | Open use, source required | – | – |
| GE | free | Open use, source required | [sitg.ge.ch](https://sitg.ge.ch/ressources/conditions-utilisation-donnees), "Données SITG" | 2017–2026 |
| GL | free | Open use | [PDF](https://www.geodienste.ch/pdfs/GL/lwb_nutzungsflaechen/data/ktgl-ogd-geo-20260622.pdf) | – |
| GR | free | – | [geo.gr.ch](https://geo.gr.ch/geodaten/nutzungsbedingungen), "Quelle: [Datenbestand], Kanton Graubünden, JJJJ" | – |
| JU | free | Open use, source required | [PDF](https://geo.jura.ch/geodonnees/Conditions_utilisation_geodonnees.pdf), "Géodonnées de la République et Canton du Jura" | – |
| LU | free | Open use, source required | [geoportal.lu.ch](https://geoportal.lu.ch/geodaten/nutzungsbedingungen) | – |
| NE | registration | Open use, source required | [PDF](https://sitn.ne.ch/geoshop2_media/documents/contrat_sitn.pdf), "Données SITN : [année] SITN http://www.ne.ch/sitn" | – |
| NW | approval | – | [PDF](https://www.gis-daten.ch/downloads/public/Richtlinien_Weisungen/Nutzungsbestimmungen_Geodaten_und_Geodienste.pdf), "Quelle: GIS Daten AG [Datum Datenbezug]" | – |
| OW | approval | – | same as NW | – |
| SG | free | – | [sg.ch](https://www.sg.ch/bauen/geoinformation/datenbezug/agb.html), §18 limits redistribution of data from open geoservices | – |
| SH | free | Open use | – | – |
| SO | free | Open use | – | – |
| SZ | free | Open use, source required | [PDF](https://www.geodienste.ch/pdfs/SZ/lwb_nutzungsflaechen/data/Open%20Data%20Lizenz%20AFL.pdf), "Amt für Landwirtschaft (AFL), Kanton Schwyz" | 2022–2024 |
| TG | free | Open use, source required | – | – |
| TI | registration | Open use, source required | [ti.ch](https://www4.ti.ch/dt/sg/sai/ugeo/temi/geoportale-ticino/geoportale/condizioni-utilizzo/), "Fonte: Amministrazione cantonale - Canton Ticino" | – |
| UR | free | Open use, source required | [lisag.ch](https://www.lisag.ch/nutzungsbestimmungen-gis-uri), "Quelle: Lisag AG" | – |
| VD | approval | – | [vd.ch](https://www.vd.ch/themes/territoire-et-construction/cadastre-et-geoinformation/geodonnees/commande-de-geodonnees/conditions-dutilisation/) | – |
| VS | free | Open use, source required | – | – |
| ZG | free | Open use, source required | [zg.ch](https://zg.ch/de/planen-bauen/geoinformation/geoinformationen-nutzen/nutzungsbedingungen), "Quelle: GIS Kanton Zug" | – |
| ZH | free | Open use | [geo.zh.ch](https://geo.zh.ch/terms-of-use) | 2017–2025 |

FL publishes no data. The opendata.swiss records of BE, FR, GE and TG say "Open use" where geodienste.ch shows
"source required"; the converters follow geodienste.ch.

### Properties

| Property                | Data Type | Constraints | Description     |
|-------------------------|-----------|-------------|-----------------|
| FID                     | number    |             | Identifier      |
| bezugsjahr              | number    |             | The year of validity |
| lnf_code                | number    |             | Code of the federal usage catalogue |
| nutzung                 | string    |             | Usage           |
| ist_ueberlagernd        | boolean   |             | Overlaps        |
| code_programm           | string    |             |                 |
| programm                | string    |             |                 |
| nutzungsidentifikator   | string    |             | Usage identifier |
| anzahl_baeume           | number    |             | Number of trees |
| bewirtschaftungsgrad    | number    |             | Degree to which the field is getting cultivated |
| beitragsberechtigt      | number    |             |                 |
| nutzung_im_beitragsjahr | number    |             |                 |
| nhg                     | boolean   |             |                 |
| ist_definitiv           | boolean   |             | is final        |
| verpflichtung_von       | number    |             |                 |
| verpflichtung_bis       | number    |             |                 |
| schnittzeitpunkt        | string    |             |                 |
| identifikator_be        | string    |             |                 |
| flaeche_m2              | int       |             | area in sq. meter |
| kanton                  | string    |             | Canton code     |

### Example

An impression (with crop categories) can be seen on the Swiss geoportal map: https://s.geo.admin.ch/zoa4b9lok3g8
