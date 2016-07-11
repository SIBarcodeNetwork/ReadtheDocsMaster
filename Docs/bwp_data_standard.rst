BWP Data Standard Extension
===========================

The Barcode of Wildlife Data Standard Extension was created by the BWP Specimen Informatics Working Group to hold the barcode records from BWP to the higher level required for using as evidence in court cases.

Relation to Barcode Data Standard
---------------------------------

The first component of the BWP Data Standard states that all "strongly recommended" elements from the Barcode Data Standard are now required. These elements include:
	
	* latitude/longitude
	* name of identifier
	* name of collector
	* collection date
	* PCR primer names

New fields in the BWP Structured Comment
----------------------------------------

In addition to the newly required fields listed above, BWP worked with GenBank to create a standardized BWP "structured comment", which will contain these extra fields in BWP Barcode GenBank records.

.. image:: /images/bwp_structured_comment.png
  :align: center
  :target: /en/latest/_images/bwp_structured_comment.png

basisOfIdentification -- Required
	Free-text field describing what rationale was used to identify the specimen voucher as representing the Taxon. Can include materials examined or reference specimens, literature, or field guides.

identificationConfidence -- Required
	The subjective appraisal by the identifier of the reliability of the identification at the species level. The reliability of a species identification can be High, Medium or Preliminary, based on the identifier’s expertise in the taxonomic group, the nature and quality of the specimen, and the reference material used to make the identification.

identificationDate -- Required
	The date on which the specimen voucher was identified as representing the Taxon.

typeStatus -- Required
	A list (concatenated by semicolons) of nomenclatural types (type status, typified scientific name, publication) applied to the subject. DarwinCore recommends a controlled vocabulary of none, holotype, paratype, neotype, syntype, lectotype, paralectotype, hapantotype, other.

chainOfCustody -- Optional
	Whether or not a specimen voucher has been collected, transported, and accessioned into a secure repository following chain of custody rules that prevent tampering, contamination, mislabeling or loss. Chain of custody refers to the chronological documentation of the sequence of physical locations of a voucher specimen and the people who had custody of it.

coordinatePrecision -- Optional
	A decimal representation of the precision of the coordinates given in the decimalLatitude and decimalLongitude fields. This field is REQUIRED when you are giving "fuzzed" GPS coordinates. Make sure the actual real coordinates are stored in your specimen database.

	**Example**: "1.0 (nearest degree)" for when real decimalLatitude and decimalLongitude values of 38.891351 and -77.026072 are "fuzzed" to 39 and -77 to protect location information.
