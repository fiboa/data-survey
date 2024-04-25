# Data Survey

A survey of non-standardized metadata, data and APIs that describe agricultural
fields and their boundaries.

## Data

The following data has been surveyed:
- [North Rhine-Westphalia (NRW), Germany](data/DE-NRW.md)
- [Berlin / Brandenburg, Germany](data/DE-BB.md)
- [Schleswig-Holstein (SH), Germany](data/DE-SH.md)
- [Lower Saxony, Germany](data/DE-NDS.md)
- [Thuringia, Germany](data/DE-TH.md)
- [Austria: INVEKOS Referenzen Österreich 2021](data/AT.md)
- [Vlaanderen, Belgium](data/BE-Vlaanderen.md)
- [EuroCrops](data/EU-EuroCrops.md)
- [Digifarm](data/EU-Digifarm.md)
- [AI4Boundaries](data/AI4Boundaries.md)
- [Open Supply Hub](data/Open-Supply-Hub.md)
- [AI4SmallFarms (Southeast Asia)](data/VM-KH-AI4SmallFarms.md)
- [India - 10k small holder](data/IN.md)
- [Planet](data/Planet.md)
- [PASTIS](data/PASTIS.md)
- [USDA Crop Sequence Boundaries](data/US.md)
- [Global FieldID (Varda)](data/Global%20FieldID.md)


## Data Survey Instructions

In order to help everyone get a real sense of how different field boundary datasets are structured we’ve started this survey. 
The idea is to have a page for each dataset that gives an overview of the data, includes details about it (file format, 
documentation, license, projection), and lays out the data schema / metadata. Every organization that is creating or consuming 
field boundaries should contribute to this. It is ok if it is a very simple schema, like just ID and Field. 

This should provide an easy reference during the [field boundaries workshop](https://sites.google.com/view/tge-field-boundary-initiative/) 
to ground any discussion about particular attributes, as we can easily look at to see what others did. And it should also 
serve as a continued resource to others in the future (if you don’t want to publish publicly we can also accommodate you). 

See the below for instructions if you're comfortable with GitHub or you can also just use 
[this google doc template](https://docs.google.com/document/d/1MQrVOG11bT_TbdorqxS8gL1CjJBWIkdYfok0dzTIz5Q/edit) and then 
include it in a new issue.

## Contribute

- Feel strongly encouraged to submit your information for the survey via a
  [Pull Request](https://github.com/fiboa/data-survey/pulls). 
- Please use the [template.md](template.md) to fill the survey. See the examples above for inspiration.
- Place the document with a descriptive name into the [data](data/) folder.
  If you provide more than one file, please create a folder that contains all files.
- The submission should include example data, ideally in GeoJSON format.
