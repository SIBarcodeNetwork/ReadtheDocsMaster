Welcome to the SI Barcode Network Informatics Documentation!
============================================================

This documentation site describes the best practices for the informatics pipeline of the SI Barcode Network.

.. _updates-link:

Updates
-------

.. image:: https://img.shields.io/badge/Biocode%20Plugin%20Version-3.0.9-green.svg
    :target: https://github.com/biocodellc/biocode-lims/releases/download/v3.0.9/BiocodePlugin_3_0_9.gplugin

.. image:: https://img.shields.io/badge/GenBank%20Upload%20Plugin%20Version-1.6.7-green.svg
    :target: http://assets.geneious.com/plugins/GenbankSubmission_1_6_7.gplugin

6 March, 2019
	The Biocode plugin now includes the following fields: genbankCountry, genbankDate, and genbankLatLng. 

26 November, 2018
	The GenBank submission plugin was updated to version 1.6.7, correcting a few issues regarding annotations, as well as other small updates. You can view the full list of features and updates `here. <http://www.geneious.com/plugins/genbank-submission-plugin#history>`_ 

11 September, 2017
	Biocode plugin updated to fix problem where the Biocode FIMS only retrieved field definitions from the Barcode of Wildlife project instead of the project that was specified. This would result in empty tissue fields.

20 September, 2016
	The GenBank submission plugin was updated to version 1.6.5 with many minor bug fixes. The most important one to the SI Federal Barcoding Project is that the plugin will now attemp to replace non-ASCII characters (such as accented characters) with equivalent ASCII characters. This has been a problem in the past, since the previous default action was to simply omit these characters.

15 June, 2016
	The Biocode Plugin was updated to version 3.0.0, and the GenBank Upload Plugin was updated to version 1.6.4. You can read about the updates to the Biocode Plugin `here <http://software.mooreabiocode.org/index.php?title=Release_Notes#Biocode_Plugin_3.0.0_-_9_June_2016>`_. You can read about the updates to the GenBank Upload Plugin `here. <http://www.geneious.com/plugins/genbank-submission-plugin#history>`_

.. toctree::
	:caption: Background

	workflow
	software_components
	barcode_data_standard
	conventions

.. toctree::
	:maxdepth: 2
	:caption: FIMS

	fims_spreadsheet_pop
	fims_spreadsheet_val

.. toctree::
	:maxdepth: 2
	:caption: LIMS

	geneious_intro
	biocode_plugin
	extraction_plates
	pcr_plates
	cyclesequencing_plates
	
.. toctree::
	:maxdepth: 2
	:caption: Sequence Assembly and Publication

	downloading_traces
	assembling_contigs
	sequence_qc
	mark_pass

.. toctree::
	:maxdepth: 2
	:caption: Data Publication

	gb_upload
	noncoding_annotation
	rapid_data_release
	gb_update
	bioprojects
