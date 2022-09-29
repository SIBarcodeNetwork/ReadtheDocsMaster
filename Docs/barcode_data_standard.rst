Barcode Data Standard
=====================

Introduction
------------

The Barcode Data Standard was established by the Consortium of the Barcode of Life soon after the first scientific paper by Dr. Paul Hebert was published that proposed the method of DNA Barcoding. You can view and download the official data standard document `here <https://github.com/SIBarcodeNetwork/SIBarcodeNetwork/blob/master/BARCODE%20Data%20Standards%20v2.4.pdf>`_. 

	Please note that, while the GenBank keyword BARCODE is no longer actively assigned by NCBI, this document is still referred to in the attempt to create barcode quality sequence records on GenBank. The portions referring to submission of trace files are no longer applicable, as the NCBI Trace Archive has been retired.

The data standard consists of several required and strongly recommended elements that have to do either with specimen metadata or sequence data. We will go through each element, give a brief explanation, and try to highlight any commonly seen mistakes.

+----------------------------------------+---------------------+------------------------------+
| **Specimen Metadata**                                                                       |
+========================================+=====================+==============================+
| | **Text from Standard**               | **GenBank Field**   | **Required or Recommended?** |
+----------------------------------------+---------------------+------------------------------+
| | "a unique identifier for the voucher | specimen_voucher    | Required                     |
| | specimen using a structured field    |                     |                              |
| | specified by CBOL and NCBI"          |                     |                              |
+----------------------------------------+---------------------+------------------------------+
| | "the name of a formally described    | organism            | Required                     |
| | species or a provisional label for   |                     |                              |
| | an unpublished species"              |                     |                              |
+----------------------------------------+---------------------+------------------------------+
| | "Country-Code using the controlled   | country             | Required                     |
| | vocabulary used by GenBank"          |                     |                              |
+----------------------------------------+---------------------+------------------------------+
| | "Latitude and longitude"             | lat_lon             | Strongly recommended         |
+----------------------------------------+---------------------+------------------------------+
| | "Name of the identifier"             | identified_by       | Strongly recommended         |
+----------------------------------------+---------------------+------------------------------+
| | "Name of the collector"              | collected_by        | Strongly recommended         |
+----------------------------------------+---------------------+------------------------------+
| | "Date of collection"                 | collection_date     | Strongly recommended         |
+----------------------------------------+---------------------+------------------------------+
| **Sequence Metadata**                                                                       |
+----------------------------------------+---------------------+------------------------------+
| | **Text from Standard**               | **GenBank Field**   | **Required or Recommended?** |
+----------------------------------------+---------------------+------------------------------+
| | "Come from a gene region             | gene                | Required                     |
| | accepted by CBOL as an effective     |                     |                              |
| | barcode" ... "Include the name of    |                     |                              |
| | the region used"                     |                     |                              |
+----------------------------------------+---------------------+------------------------------+
| | "the sequences of all forward and    | PCR_primers         | Required                     |
| | reverse primers used"                |                     |                              |
+----------------------------------------+---------------------+------------------------------+
| | "the names of the forward and        | PCR_primers         | Strongly recommended         |
| | reverse primers"                     |                     |                              |
+----------------------------------------+---------------------+------------------------------+
| | "at least 75% contiguous, high       | nucleotide_sequence | Required                     |
| | quality bases from within the        |                     |                              |
| | approved barcode region"             |                     |                              |
+----------------------------------------+---------------------+------------------------------+

.. note::

   The full official definitions and descriptions for all of these terms can be found at on the INSDC Feature Table page at http://www.insdc.org/files/feature_table.html#7.3

Specimen metadata
-----------------

Collection metadata
~~~~~~~~~~~~~~~~~~~

Country -- Required
	The GenBank field name “Country” is slightly confusing -- not just because the INSDC country controlled vocabulary list (http://www.insdc.org/country.html) includes oceans and seas in addition to countries -- but because the country name is often concatenated with a colon to provide more specific location information about where a specimen was collected. Typically, locality terms following the standardized country name are ordered in ascending order of specificity. An example for a specimen collected on the grounds of the Smithsonian Natural History Museum might be "USA: Washington, DC; Smithsonian Natural History Museum; West Loading Dock".

Latitude and Longitude -- Strongly Recommended
	The geographical coordinates of the location of where a specimen was collected are stored in the “lat_lon” field in decimal format. GenBank uses the specific format "d[d.dddd] N|S d[dd.dddd] W|E". An example of this is "38.891262 N 77.026093 W" for the Smithsonian Natural History Museum.

Collector Name -- Strongly Recommended
	The name of the person(s) or institute that collected the specimen. GenBank does not provide any guidance on how to structure name ("Give Name Surname" vs. "Surname, Given Name") or how to group multiple names, but at least be consistent.

Collection Date -- Strongly Recommended
	The date(s) on which the specimen was collected. Date ranges are supported by providing two collection dates from among the supported value formats, delimited by a forward-slash character.

	Here are the supported value formats, with examples: 

		* "DD-Mmm-YYYY": 01-Jan-2016
		* "Mmm-YYYY": Jan-2016
		* "YYYY": 2016
		* "YYYY-MM-DD": 2016-01-01
		* "YYYY-MM": 2016-01


Voucher metadata
~~~~~~~~~~~~~~~~

Specimen Voucher -- Required
	The specimen voucher field is the most important portion of the Barcode Data Standard, because it serves as the bridge between genetic data and specimen data. This field is even more important for plants, because the plant barcode consists of more than one gene region. The two sequences that make up a plant barcode are published as two separate GenBank records, so a unique specimen voucher field is the only thing that asserts that these sequences came from the same individual.
	
	Not only is a unique identifier required for the specimen voucher, but it also needs to be in a specific format. It is very easy to miss since this format is specified in a footnote, but the data standard document specifies that the voucher specimen identifier should use a triplet structure based on elements of the Darwin Core (DwC) separated by a colon::

		institutionCode:collectionCode:catalogNumber
		
	There are also instances where the voucher specimen identifier uses a doublet separated by a colon, such as in the cases of botanical collections in herbaria. For example, the doublet US:12345678 would represent a voucher specimen in the United States National Herbarium, where the code US represents both institution code and collection code.

	To ensure that specimen voucher identifiers are unique and traceable, GBIF maintains the GBIF Registry of Scientific Collections (`GBIF.org <https://www.gbif.org/grscicoll/>`_), which builds on GRSciColl, a comprehensive, community-curated clearinghouse of collections information originally developed by Consortium of the Barcode of Life (CBOL).

Organism -- Required
	The scientific name of the organism that provided the sequenced genetic material. The text from the data standard reads "the name of a formally described species or a provisional label for an unpublished species", which allows for the exception of allowing for organism names only identified to the Order or Family level. It is recommended by GenBank to give provisional names the values of the specimen voucher for reproducibility reasons.

Identifier Name -- Highly Recommended
	The name of the person(s) or institute that identified the specimen. Just as with Collector Name, GenBank does not provide any guidance on how to structure name ("Give Name Surname" vs. "Surname, Given Name") or how to group multiple names, but at least be consistent.

Sequence metadata
-----------------

Nucleotide Sequence -- Required
	This is the DNA sequence of the barcode record.

PCR Primer Sequence(s) -- Required
	This refers to the sequences for the PCR primers used to amplify the DNA Barcode region. All sequences should be presented in 5'>3' order.

PCR Primer Name(s) -- Highly Recommended
	This refers to the "common names" of the primer sequences. Unfortunately this field is optional, and the vast majority of barcode records do not have primer names listed.

Trace Files -- Optional
	If desired, trace files for the forward and reverse sequencing runs may be submitted to the NCBI Sequence Read Archive (SRA). See https://www.ncbi.nlm.nih.gov/sra/docs/submitformats/ for further information.	
