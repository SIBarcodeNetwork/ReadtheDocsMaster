Generating Cycle Sequencing Plates
==================================

Creating the Plate
------------------

To append new cycle sequencing reactions onto existing PCR workflows, follow the :ref:`biocode_plugin-link` page to log onto the Biocode Plugin. Search for the corresponding PCR plate.

.. figure:: /images/search_results_CS.png
  :align: center 

Highlight the PCR plate that is brought up from the search and click "New Reaction" in the Geneious Prime Toolbar.

.. figure:: /images/create_CS_plate.png
  :align: center

Select "Create plate from existing document" in the *New Reaction* window. 

Also select "Cycle Sequencing" from the dropdown menu for "Type of reaction". Click "OK". A cycle sequencing plate, similar to a PCR plate, will be generated. 

.. figure:: /images/empty_CS_plate.png
  :align: center

Like with PCR plates, enter a plate name in the box provided in the *New CycleSequencing* window. This name should be descriptive and unique to allow easy and successful searching in the LIMS. (See :ref:`lims_conventions-link`)

On the *New CycleSequencing* window, set the thermocycling profile in the same manner as the PCR plate.

Select "Edit All Wells" in the upper right of the *New CycleSequencing* window.

.. figure:: /images/edit_CS_wells.png
  :align: center

In the *Edit Wells* window, be sure to set the direction as Forward or Reverse.

As described for PCR plates, set the reaction cocktail, primer, date etc. "Cleanup method" will typically be "Sephadex".
 
Add any additional comments in the Notes section of the *Edit Wells* window, including which thermocycler was used, as well as the "Full Plate Label" field submitted in Signout (on labdb.si.edu - this inlcudes the number Signout assigned to the plate when submitted for sequencing).

If the cycle sequencing plate contains reactions for both directions, then highlight the forward reaction wells, click on "Edit Selected Wells" on the top right of the *New CycleSequencing* window and set the direction and primer. Do the same for the remaining reaction wells in the opposite direction.

Attaching Raw Traces to a Cycle Sequencing Plate
------------------------------------------------

Single Trace Upload
~~~~~~~~~~~~~~~~~~~~

To add a trace file to a single cycle sequencing reaction:

Double click to open the reaction well of interest in the *New CycleSequencing* window.  

.. figure:: /images/edit_CS_wells_addtrace.png
  :align: center

In the *Edit Wells* window that now appears, select the "Add/Edit Traces" button. This option only appears if a single well was selected and opened.

.. figure:: /images/add_trace_well.png
  :align: center

A new window will appear with an "Add Sequence(s)" button located in the upper left corner of the window. 

Click the button and direct Geneious to the location of the raw trace file. Be sure to add only the correct trace (e.g. forward or reverse) to each reaction. 

To remove one or more traces from a single well, select the trace or traces in question and click "Remove Sequence(s)".

Bulk Trace Upload
~~~~~~~~~~~~~~~~~~

To bulk upload traces to a cycle sequencing plate or set of reactions:

In the *New CycleSequencing* window, click "Bulk Add Traces" on upper right of the window. 

Click "Browse" to point Geneious to the location of the trace files. Traces are matched to their corresponding cycle sequencing reactions based on components found in the trace file name (i.e., well number or field) along with name delimiters. For example, to attach a sample’s trace file to it’s corresponding well position based on the well position in the trace file name (for example, trace name 3726294 _\ **A01**\ _capture.ab1), the user would select the "Well number" option followed by "Match 2nd part of name", "separated by_(Underscore)" in the *Bulk add traces* window.

.. figure:: /images/bulk_add_traces_well.png
  :align: center 

To attach a sample’s trace file based on a field (in the above example, trace name **3726294**\ _A01_capture.ab1), the user would select the "Field" button followed by "Extraction Barcode" from the dropdown menu along with "Match 1st part of name, separated by _(Underscore)".

.. figure:: /images/bulk_add_traces_field.png
  :align: center 

After all traces have been attached, click "OK" to create and save the cycle sequencing plate. 

To double check that the traces have successfully attached the user can change the display options of the cycle sequencing plate so that # Traces is displayed. If the traces have attached correctly, wells should display "# Traces: 1".

.. figure:: /images/cycseq_display_number_traces.png
  :align: center 

With the traces now attached to their corresponding cycle sequencing reaction plates, they are ready to be used by the Geneious Assembler. See :ref:`trace_download-link` instructions to begin the assembly process.
