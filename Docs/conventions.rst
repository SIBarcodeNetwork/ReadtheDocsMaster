Naming conventions
==================

.. _conventions-link:

FIMS naming conventions
-----------------------

Once specimens are available to be processed in the lab, you must divide the specimens into a batch, or batches, of specimens that will be processed together through the full laboratory pipeline (extraction through to sequencing). Each batch is also known as a "plate" or "dataset", terms that will be used repeatedly throughout our instructions for the FIMS and LIMS. Specimen spreadsheets must be completed for each plate of specimens prior to their processing in the lab. 

Create your plate/dataset name from [Institution Code]_[User Initials]_[Sequential Number]
	Example: CBOL_MGT_001 for the first plate/batch from Michael G Trizna of CBOL

This name will then be used for the:

* Spreadsheet filename (CBOL_MGT_001.xlsx)

* Dataset Code in FIMS

.. image:: /images/dataset_code.png
	:align: center

* extractionPlateID field in spreadsheet

.. image:: /images/plateid.png
	:align: center
	
* and will also be incorporated in the plate names in the LIMS system (see below)

.. _lims_conventions-link:

LIMS naming conventions
-----------------------

Extraction Plate:
	*[dataset code]_X[extraction attempt number]*

	Example: CBOL_MGT_001_X01 for the first extraction plate from the plate/batch of samples in the dataset named “CBOL_MGT_001”. If you were to re-extract DNA from all of the samples in CBOL_MGT_001, then this second extraction plate would be called CBOL_MGT_001_X02.


PCR Plate:
	*[dataset code]_PCR[PCR attempt number]_[fwd primer]_[rev primer]*

	Example: CBOL_MGT_001_PCR01_dgLCO1490_dgHCO2198 for a PCR reaction of the CBOL_MGT_001 plate using primers dgLCO1490 and dgHCO2198. Subsequent PCRs should be named in chronological order regardless of the primer set used. For example if a second PCR was completed for this plate it would be named CBOL_MGT_001_PCR02_Fprimername_Rprimername.


Cycle Sequencing Plate:
	*[dataset code]_Seq[Sequencing attempt number]_[primer used]_[F or R]*

	Examples: CBOL_MGT_001_Seq01_dgLCO1490_F for the cycle sequencing plate for the forward strand using the dgLC01490 primer; and CBOL_MGT_001_Seq02_dgHCO2198_R for the reverse strand using the dgHCO2198 primer. 
	
	

*IMPORTANT* There are different scenarios for dealing with re-runs (extractions, PCRs and sequencing) of subsets of samples from an individual dataset. Please contact us to discuss these scenarios to ensure that you continue to use a manageable workflow in the LIMS.
