Naming Conventions
==================

.. _conventions-link:

FIMS Naming Conventions
-----------------------

Once tissues are available to be processed in the lab, they are divided into a batch, or batches, of tissues that will be processed together through the full laboratory pipeline (extraction through to sequencing). Each batch is also known as a “plate” and is saved as an “expedition” in the GEOME FIMS database. These terms will be used repeatedly throughout our instructions for the FIMS and LIMS. Specimen spreadsheets must be completed for each plate of tissues prior to their processing in the lab. 

The SI Barcode Network creates the expedition name from [Fiscal Year][Project Abbreviation]
	Example: FY19Orthoptera for the Orthopterans project from Fiscal Year 2019

This name will then be used for the:

* Expedition Title

* Expedition Code

.. image:: /images/dataset_code.png
	:align: center
	:scale: 50 %

The SI Barcode Network creates the plate name from [Expedition Name]_P[Sequential Number]
	Example: FY19Orthoptera_P01 for the first plate/batch from the Orthopterans project from Fiscal Year 2019

This name corresponds to the plate name in the lab and will be used for the tissuePlate field in the FIMS spreadsheet: 

.. image:: /images/plateid.png
	:align: center
	:scale: 50 %
	
This name will also be used in the LIMS system (see below)

.. _lims_conventions-link:

LIMS Naming Conventions
-----------------------

Extraction Plate:
	*[plate name]_X[extraction attempt number]*

	Example: FY19Orthoptera_P01_X01 for the first extraction plate from the plate/batch of samples in the expedition named “FY19Orthoptera_P01”. If DNAs of all samples in FY19Orthoptera_P01 were re-extracted, then the second extraction plate would be called FY19Orthoptera_P01_X02.

Working Stock of Extraction Plate:
	*[plate name]_X[extraction attempt number][working stock number]*

	Example: FY19Orthoptera_P01_X01_W01 for the first working stock plate created from the FY19Orthoptera_P01_X01 extraction plate. A second working stock from this same extraction plate would be named FY19Orthoptera_P01_X01_W02.

PCR Plate:
	*[plate name]_PCR[PCR attempt number]_[fwd primer]_[rev primer]*

	Example: FY19Orthoptera_P01_PCR01_dgLCO_dgHCO for a PCR reaction of the FY19Orthoptera_P01 plate using primers dgLCO1490 and dgHCO2198. Subsequent PCRs should be named in chronological order regardless of the primer set used. For example if a second PCR was completed for this plate it would be named FY19Orthoptera_P01_PCR02_Fprimername_Rprimername.


Cycle Sequencing Plate:
	*[plate name]_Seq[Sequencing attempt number]_[primer used]_[F or R]*

	Examples: FY19Orthoptera_P01_Seq01_dgLCO_F for the cycle sequencing plate for the forward strand using the dgLC01490 primer; and FY19Orthoptera_P01_Seq01_dgHCO_R for the reverse strand using the dgHCO2198 primer. 

Reruns Plate:
	*[expedition code]_Reruns_[plate number]*

	Example: 144 samples from the FY19Orthoptera expedition have been cherry picked into two rerun plates. The first plate will be called “FY19Orthoptera_Reruns_P01” and the second will be called “FY19Orthoptera_Reruns_P02”. 

	
