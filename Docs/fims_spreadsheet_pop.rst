Populating the GeOMe FIMS spreadsheet
===============================

The GeOMe FIMS spreadsheet template
-----------------------------

The SI Barcode Network GeOMe FIMS spreadsheet template is hosted on the SI Barcode Network GitHub page at https://github.com/SIBarcodeNetwork/SIBarcodeNetwork, called "SI Barcoding Specimen Spreadsheet.xlsx". (The direct link to download it is `here <https://github.com/SIBarcodeNetwork/SIBarcodeNetwork/raw/master/SI%20Barcoding%20Specimen%20Spreadsheet.xlsx>`_.) If you would like to personalize the columns included in your template, you also have the option to generate it directly through GeOMe, by following `this link <https://geome-db.org/workbench/template>`_.

.. figure:: /images/spreadsheet_on_github.png
  :align: center
  :target: /en/latest/_images/spreadsheet_on_github.png

  This screenshot of the SIBarcodeNetwork GitHub page shows the location of the specimen spreadsheet template.

It is a good idea to immediately rename this spreadsheet file with the name of your dataset according to the :ref:`conventions-link`.

.. figure:: /images/sibn_spreadsheet_template.png
  :align: center
  :target: /en/latest/_images/sibn_spreadsheet_template.png

  This screenshot shows a portion of the column headers of the specimen spreadsheet template.

There are four tabs in the spreadsheet: Instructions, Samples, Samples_Fields, and Lists. The Instructions tab explains how to use and populate the spreadsheet. The Samples tab is where your data will be entered. The Samples_Fields tab includes definitions for all the columns on the Samples tab. The Lists tab includes all controlled vocabulary for certain fields. 

Source of columns
~~~~~~~~~~~~~~~~~

The GeOMe FIMS, which we will be using to store and interface with specimen data, allows projects to completely customize the fields that they use -- along with the validation rules that accompany those fields. Since the goal of the SI Barcode Network is to get BARCODE keyword sequences into GenBank, we limited the specimen fields to those that will end up in a GenBank record. However, we also based our fields on `DarwinCore <http://rs.tdwg.org/dwc/terms/#dcindex>`_ fields, which you should notice in the field names. We think that our collections of fields act as a bridge between permanent collection databases (like `NMNH EMu <http://collections.nmnh.si.edu/search/>`_) and GenBank.

Column colors
~~~~~~~~~~~~~

Red column headers indicate fields required before they can be uploaded to the FIMS. 
Black column headers are not required, but they should still be filled out if the values are known.

Column definitions
------------------

materialSampleID 
  The collector's specimen number. This number must be unique among the IDs within the expedition. You can use the field number or voucherCatalogNumber, if no field number exists.

institutionCode 
  This is the acronym for the institution or repository where the specimen voucher is stored. `The Global Registry of Scientific Collections <https://www.gbif.org/grscicoll/institution/search>`_ is a registry for all institution codes, and the institutionCode field will be validated against its list of codes. Vouchers accessioned at the Smithsonian will usually have the institutionCode “USNM”.

collectionCode    
  The name, acronym, coden, or initialism identifying the collection or data set from which the record was derived. This collectionCode should be registered, along with the institutionCode, in `The Global Registry of Scientific Collections <https://www.gbif.org/grscicoll/institution/search>`_.

catalogNumber          
  An identifier (preferably unique) for the record within the data set or collection.

voucherCatalogNumber        
  This is the unique id given to the specimen the tissue was taken from. It is constructed from the institutionCode, collectionCode (if one exists), and catalogNumber, joined by a colon (:).

kingdom         
  The full scientific name of the kingdom in which the taxon is classified.

phylum   
  The full scientific name of the phylum in which the taxon is classified. The list of phyla allowable in GeOMe are taken from the Catalog of Life.  In addition, we have added 'Unknown' as an acceptable value. See controlled vocabulary in the Lists tab of the spreadsheet. 

class    
  The full scientific name of the class in which the taxon is classified.

order
  The full scientific name of the order in which the taxon is classified.

family
  The full scientific name of the family in which the taxon is classified.

genus
  The full scientific name of the genus in which the taxon is classified.

specificEpithet
  The full scientific name of the specificEpithet in which the taxon is classified.

scientificName
  The full scientific name of the specimen. When forming part of an Identification, this should be the name in lowest level taxonomic rank that can be determined.

identifiedBy
  A list (concatenated and separated by the pipe ('|') symbol) of names of people, groups, or organizations who assigned the Taxon to the subject.

collectorList
  A list (concatenated and separated by the pipe ('|') symbol) of names of people, groups, or organizations responsible for recording the original Occurrence. The primary collector or observer, especially one who applies a personal identifier (recordNumber), should be listed first.

yearCollected
  The four-digit year in which the voucher was collected, according to the Common Era Calendar. (If you are unsure of the value and will never come across it, add ‘Unknown’, or if you do not currently have the data but will in the future, add ‘TBD’.)

monthCollected
  The two-digit numerical month in which the voucher was collected. This will be validated to being in the range from 1 to 12.

dayCollected
  The integer day of the month on which the voucher was collected. This will be validated to being in the range from 1 to 31.

country
  The name of the country or major administrative unit in which the Location occurs. This field will be validated against the INSDC country list (http://www.insdc.org/country.html). See controlled vocabulary in the Lists tab of the spreadsheet. 

locality
  The specific description of the collection location. Less specific geographic information can be provided in other geographic terms (higherGeography, continent, country, stateProvince, county, municipality, waterBody, island, islandGroup). This term may contain information modified from the original to correct perceived errors or standardize the description. (If you are unsure of the value and will never come across it, add ‘Unknown’, or if you do not currently have the data but will in the future, add ‘TBD’.) This will be combined with the countryOrOcean field in the GenBank record.

decimalLatitude
  The geographic latitude (in decimal degrees, using the spatial reference system given in geodeticDatum) of the geographic center of a Location. Positive values are north of the Equator, negative values are south of it. Legal values lie between -90 and 90, inclusive.

decimalLongitude
  The geographic longitude (in decimal degrees, using the spatial reference system given in geodeticDatum) of the geographic center of a Location. Positive values are east of the Greenwich Meridian, negative values are west of it. Legal values lie between -180 and 180, inclusive.

tissueType
  A list (concatenated and separated) of the tissue types sampled from this individual, together with any tissue identifiers that were assigned to them

tissuePlate
  The name of the plate (typically a 96 well plate) containing the tissue subsamples that will be consumed for DNA extractions for projects.

tissueWell
  The well location in the tissue plate – formatted as follows: A01, A02, etc. 

tissueID
  This is the unique identifier for the tissue sample from which the DNA was extracted. This identifier must be unique across all projects. The materialSampleID can be used. If there are multiples of a tissue sample in different wells, please use the following format: materialSampleID + “.#”, where “#” is the number corresponding to the multiple (e.g. “.1” for the first occurrence, “.2” for the second occurrence).

tissueOtherCatalogNumbers
  This is the 2D barcode of the storage tube which contains the DNA extract of the specimen. This field will not be populated until after the DNA extraction process is complete.

boldProcessID
  BOLD Process IDs are unique codes automatically generated for each new record added to a project within the Barcode of Life Database.

