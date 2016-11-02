Populating the FIMS spreadsheet
===============================

The FIMS spreadsheet template
-----------------------------

The SI Barcode Network FIMS spreadsheet template is hosted on the SI Barcode Network GitHub page at https://github.com/MikeTrizna/SIBarcodeNetwork, called "SI Barcoding Specimen Spreadsheet.xlsx". You can also download the spreadsheet directly from `here <https://github.com/MikeTrizna/SIBarcodeNetwork/raw/master/SI%20Barcoding%20Specimen%20Spreadsheet.xlsx>`_.

.. figure:: /images/spreadsheet_on_github.png
  :align: center
  :target: /en/latest/_images/spreadsheet_on_github.png

  This screenshot of the SIBarcodeNetwork GitHub page shows the location of the specimen spreadsheet template.

It is a good idea to immediately rename this spreadsheet file with the name of your dataset according to the :ref:`conventions-link`.

.. figure:: /images/sibn_spreadsheet_template.png
  :align: center
  :target: /en/latest/_images/sibn_spreadsheet_template.png

  This screenshot shows a portion of the column headers of the specimen spreadsheet template.

Source of columns
~~~~~~~~~~~~~~~~~

The BiSciCol FIMS, which we will be using to store and interface with specimen data, allows projects to completely customize the fields that they use -- along with the validation rules that accompany those fields. Since the goal of the SI Barcode Network is to get BARCODE keyword sequences into GenBank, we limited the specimen fields to those that will end up in a GenBank record. However, we also based our fields on `DarwinCore <http://rs.tdwg.org/dwc/terms/#dcindex>`_ fields, which you should notice in the field names. We think that our collections of fields act as a bridge between permanent collection databases (like `NMNH EMu <http://collections.nmnh.si.edu/search/>`_) and GenBank.

Column colors
~~~~~~~~~~~~~

Blue column headers are all identifiers of either the specimen voucher, the tissue sample of the voucher, or the DNA extraction from that tissue. Green column headers are all specimen metadata about the collection event or taxonomic identification of the specimen. Finally, red fields will be populated by CBOL staff after the spreadsheet has been completed.

Dark-colored column headers indicate fields required before they can be uploaded to the FIMS. Light-colored column headers are not required, but they should still be filled out if the values are known.

Column definitions
------------------

extractionPlateID 
  Name of the DNA extraction plate. This will be the same as the FIMS Dataset Code.

extractionBarcode 
  This is the 2D barcode of the storage tube which contains the DNA extract of the specimen. This field will not be populated until after the DNA extraction process is complete.

extractionWell    
  This is the plate position of the DNA extraction.

tissueID          
  This is the unique identifier for the tissue sample from which the DNA extraction was taken. **This identifier must be unique across all projects.** If the tissue is stored in the NMNH Biorepository, please use the Biorepository ID. If there are multiples of a tissue sample in different wells, add a letter to distinguish them.

tissueType        
  The type of tissue that the DNA was extracted from.

voucherID         
  This is the unique id given to the specimen the tissue was taken from. It is constructed from the institutionCode, collectionCode (if one exists), and catalogNumber, joined by a colon (:).

institutionCode   
  This is the acronym for the institution or repository where the specimen voucher is stored. GRBio.org is a registry for all institution codes, and the institutionCode field will be validated against its list of codes. Vouchers accessioned at the Smithsonian will usually have the institutionCode "USNM".

collectionCode    
  The name or acronym identifying the collection or data set (from the institution/repository listed in institutionCode) from which the record was derived. This collectionCode should be registered, along with the institutionCode, in GRBio.org.

catalogNumber     
  An identifier (preferably unique) for the record within the data set or collection.

scientificName    
  The full scientific name of the specimen. When forming part of an Identification, this should be the name in lowest level taxonomic rank that can be determined.

countryOrOcean    
  The country or water body from which the specimen voucher was collected. This field will be validated against the INSDC country list (http://www.insdc.org/country.html).

locality          
  The full geographic description (within the Country or Ocean) of where the specimen was collected. This will be combined with the countryOrOcean field in the GenBank record.

decimalLatitude   
  The geographic latitude,in decimal degrees of the geographic center of a Location. Positive values are north of the Equator, negative values are south of it. This field will be validated to being within the range -90.0 to 90.0.

decimalLongitude  
  The geographic longitude,in decimal degrees of the geographic center of a Location. Positive values are east of the Greenwich Meridian, negative values are west of it. This field will be validated to being within the range -180.0 to 180.0.

yearCollected     
  The four-digit year in which the voucher was collected, according to the Common Era Calendar.

monthCollected    
  The two-digit numerical month in which the voucher was collected. This will be validated to being in the range from 1 to 12.

dayCollected      
  The integer day of the month on which the voucher was collected. This will be validated to being in the range from 1 to 31.

collectedBy       
  A list (concatenated and separated by semicolons) of names of people, groups, or organizations responsible for collecting the specimen voucher. The primary collector or observer, especially one who applies a personal identifier (recordNumber), should be listed first. The name format should preferably be Given Name, [space], Last Name.

identifiedBy      
  A list (concatenated by semicolons) of names of people who assigned the Taxon to the specimen voucher. The name format should preferably be Given Name, [space], Last Name.

kingdom           
  The full scientific name of the kingdom in which the specimen voucher is classified.

phylum            
  The full scientific name of the phylum in which the specimen voucher is classified.

class             
  The full scientific name of the class in which the specimen voucher is classified.

order             
  The full scientific name of the order in which the specimen voucher is classified.

family            
  The full scientific name of the family in which the specimen voucher is classified.

genus             
  The full scientific name of the genus in which the taxon is classified.

species           
  The name of the first or species epithet of the scientificName of the specimen voucher.

subspecies        
  The name of the lowest or terminal infraspecific epithet of the scientificName, excluding any rank designation.

gb_lat_lon        
  We use this field to combine the decimalLatitude and decimalLongitude together, since it is a single field in GenBank.

gb_country        
  We use this field to combine the CountryOrOcean and Locality fields together, since it is a single field in GenBank.

gb_collection_date
  We use this field to combine the YearCollected, MonthCollected, and DayCollected fields together, since it is a single field in GenBank.