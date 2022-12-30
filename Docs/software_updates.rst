.. _updates-link:

Software Updates
=================

.. image:: https://img.shields.io/badge/Biocode%20Plugin%20Version-3.0.18-green.svg
    :target: https://github.com/biocodellc/biocode-lims/releases/download/v3.0.18/BiocodePlugin_3_0_18.gplugin

.. image:: https://img.shields.io/badge/GenBank%20Upload%20Plugin%20Version-1.6.8-green.svg
    :target: https://assets.geneious.com/plugins/GenbankSubmission_1_6_8.gplugin

27 December, 2022
	The Biocode Plugin was updated to include performance improvements when opening the detail view of a LIMS plate. Now faster than with previous versions of the plugin. A bug was also fixed where app crashed with null latitude or null longitude.

21 November, 2022
	The Biocode Plugin was updated to incorporate the following things:
	
	* Fixed error messaging to be more descriptive when FIMS or LIMS connections do not work. This should help users diagnose connection issues themselves.
	* Fixed issue where BOLD export crashed when forward/reverse primer names were null. New behaviour asks user to name them prior to submission.
	* Added descriptive text to all options in plugin dropdown menu.
	* Changed view of wells to be A01, B01 instead of A1, B1 in table view and exports.
	* Implemented sorting function to sort wells like A01, B01, C01, instead of A01, A02, A03.
	* Updated ordering of Advanced search options to put search options that are faster at the top of the list. Helps user select options for faster searches. Equals, Begins With, and Ends With are FAR faster than contains searches. Note that these search options are available when clicking "More Options".
	* Updated list of FIMS connections to only contain working FIMS connections.
	* Upgraded development environnment to synchronize with geneious prime and java 11.

24 August, 2022
	The Biocode Plugin was updated to correct contact email for asking for help, and "tentative" was added to the list of reaction statuses, in addition to "passed" or "failed". Tentative to be used in cases where we may still need to check taxonomy but sequence is OK. Note that you should not be able to mark as "submitted" while in "tentative".

24 February, 2021
	The Biocode plugin was updated to fix issues with large tissue queries against GEOME failing. 

15 February, 2021
	The Genbank submission plugin was updated to version 1.6.8, to include substitution of disallowed characters with hyphens to prevent submission failure, and an improved error message regarding non-ASCII characters.

1 October, 2020
	The Biocode plugin was updated to fix an issue with detecting duplicate column names when annotating with FIMS data.

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
