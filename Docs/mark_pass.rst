.. _mark_pass-link:

Reaction Status in LIMS
=======================

The Reaction Status, or the "Progress" field in Biocode LIMS, can be marked as "Pass", "Tentative", or "Fail" through the Biocode Plugin menu in Geneious Prime. When Reaction Status has been marked in LIMS, the assembled contigs and consensus sequences of the marked documents become available for searching within LIMS. 

The user should also mark sequences as "Submitted" in LIMS if the sequence has been published to a public database. 

.. figure:: /images/biocode_reaction_status.png
  :align: center 
  :target: /en/latest/_images/biocode_reaction_status.png

Definitions of each status are as follows:

**Pass**: Sequence has been checked for both quality and taxonomic accuracy and is ready for submission to public databases such as GenBank.

**Tentative**: Sequence has been checked only for quality - taxonomy is still under scrutiny.

**Fail**: Sequence has been checked for either quality and failed to meet barcode data standards, or for taxonomic accuracy and is a contaminent. It will not be pushed to public databases.

**Submitted**: Sequence has been submitted to a public database (e.g. GenBank, BOLD, etc.). The sequence must first have been marked as "Pass".

Only mark **assembled contigs** as Pass, Tentative, or Fail, as that will push the data to both cycle sequencing plates in the LIMS. Marking the Reaction Status from consensus sequences will require setting read direction and then will only mark a value on one of the Cycle sequencing plates in LIMS (whichever read direction was chosen).

It is recommended that contigs are updated with current FIMS/LIMS data prior to marking the Reaction Status, to ensure the most current data is associated with the sequence in LIMS. See :ref:`Annotating_FIMS_LIMS-link` page for instruction on how to annotate assembled contigs.

Mark as Pass in LIMS
---------------------

Log in to the Biocode Plugin (see :ref:`biocode_plugin-link`)

Select the assembled contigs to be passed in LIMS.

Select the "Biocode" Icon on the Geneious Prime Toolbar and then "Mark as Pass in LIMS...." from the dropdown menu. A new window will appear.

.. figure:: /images/mark_pass.png
  :align: center 
  :target: /en/latest/_images/mark_pass.png

Leave the "Remove previous final sequencing results" box checked.

Uncheck "Also attach raw traces to sequencing reactions in LIMS".

Add any relevant notes, such as taxonomy confidence level, in the notes field under the user name. These comments will be stored within the LIMS field "Assembly Notes".

Leave the rest of the fields as the default selection, and click "OK" for the operation to run.

Mark as Tentative in LIMS
---------------------------

Log into the Biocode Plugin.

Select assembled contigs to be marked as tentative in LIMS.

Select the "Biocode" icon on the Geneious Prime Toolbar and then "Mark as Tentative in LIMS...." from the dropdown menu. A new window will appear.

.. figure:: /images/mark_tentative.png
  :align: center 
  :target: /en/latest/_images/mark_tentative.png

Leave the "Remove previous final sequencing results" box checked.

Uncheck "Also attach raw traces to sequencing reaction in LIMS".

Add any relevant notes, such as taxonomy confidence level, in the notes field under the user name. These comments will be stored within the LIMS field "Assembly Notes".

Leave the rest of the fields as the default selection, and click "OK" for the operation to run.
  
Mark as Fail in LIMS
---------------------

Once final sequences have been marked as ‘Passed’ in LIMS, failed sequences should also be marked in LIMS in the same manner:

Log onto the Biocode Plugin.

Select failed assembled contigs.

Select the "Biocode" icon on the Geneious Prime Toolbar and then "Mark as Fail in LIMS...." from the dropdown menu. A new window will appear.

.. figure:: /images/mark_fail.png
  :align: center 
  :target: /en/latest/_images/mark_fail.png

Leave the "Remove previous final sequencing results" box checked.

Uncheck "Also attach raw traces to sequencing reaction in LIMS".

Fill in the "Reason Details" and "Notes" fields with any relevant information.

Leave the rest of the fields as the default selection, and click "OK" for the operation to run.
  
Mark as Submitted in LIMS
---------------------------

Once previously passed sequences have been submitted to a public database, mark these same sequences as submitted in LIMS.

Log onto the Biocode Plugin.

Select the assembled contigs from which sequences were submitted.

Select the "Biocode" icon on the Geneious Prime Toolbar and then "Mark as Submitted in LIMS..." from the dropdown menu.

.. figure:: /images/mark_submitted.png
  :align: center 
  :target: /en/latest/_images/mark_submitted.png

In the window that appears, select "Submitted" from the dropdown menu and click "OK" for operation to run.

