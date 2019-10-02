Naming conventions
==================

.. _conventions-link:

FIMS naming conventions
-----------------------

Once tissues are available to be processed in the lab, they are divided into a batch, or batches, of tissues that will be processed together through the full laboratory pipeline (extraction through to sequencing). Each batch is also known as a "plate" or "dataset", terms that will be used repeatedly throughout our instructions for the FIMS and LIMS. Specimen spreadsheets must be completed for each plate of tissues prior to their processing in the lab. 

The SI Barcode Network creates the plate/dataset name from [Fiscal Year][Project Abbreviation]_P[Sequential Number]
	Example: FY19Ortho_P01 for the first plate/batch from the Orthopterans project from Fiscal Year 2019

This name will then be used for the:

* Spreadsheet filename (FY19Ortho_P01.xlsx)

* Expedition Code in FIMS

.. image:: /images/dataset_code.png
	:align: center
	:scale: 50 %

* extractionPlateID field in spreadsheet

.. image:: /images/plateid.png
	:align: center
	:scale: 70 %
	
* and will also be incorporated in the plate names in the LIMS system (see below)

.. _lims_conventions-link:

LIMS naming conventions
-----------------------

Extraction Plate:
	*[dataset code]_X[extraction attempt number]*

	Example: FY19Ortho_P01_X01 for the first extraction plate from the plate/batch of samples in the dataset named “FY19Ortho_P01”. If you were to re-extract DNA from all of the samples in FY19Ortho_P01, then this second extraction plate would be called FY19Ortho_P01_X02.


PCR Plate:
	*[dataset code]_PCR[PCR attempt number]_[fwd primer]_[rev primer]*

	Example: FY19Ortho_P01_PCR01_dgLCO_dgHCO for a PCR reaction of the FY19Ortho_P01 plate using primers dgLCO1490 and dgHCO2198. Subsequent PCRs should be named in chronological order regardless of the primer set used. For example if a second PCR was completed for this plate it would be named FY19Ortho_P01_PCR02_Fprimername_Rprimername.


Cycle Sequencing Plate:
	*[dataset code]_Seq[Sequencing attempt number]_[primer used]_[F or R]*

	Examples: FY19Ortho_P01_Seq01_dgLCO_F for the cycle sequencing plate for the forward strand using the dgLC01490 primer; and FY19Ortho_P01_Seq01_dgHCO_R for the reverse strand using the dgHCO2198 primer. 
	
