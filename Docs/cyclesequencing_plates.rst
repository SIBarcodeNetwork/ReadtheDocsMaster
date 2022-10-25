Generating Cycle Sequencing Plates
==================================

Creating the Plate
------------------

To append new cycle sequencing reactions onto existing PCR workflows, log onto the Biocode Plugin ( and search for corresponding PCR plate. See :ref:`search_for_plates-link` for instructions.

Highlight the PCR plate that is brought up from the search and click "New Reaction" in the Geneious Primer Toolbar.

Select "Create plate from existing document" in the *New Reaction* window. 

Also select "Cycle Sequencing" from the dropdown menu for "Type of reaction". Click "Ok". A cycle sequencing plate, similar to a PCR plate, will be generated. 
* Cycle sequencing plates can be edited in the same manner as PCR plates are edited using the *Edit Wells* window.
* As described for PCR plates, set the thermocycling profile, reaction cocktail, primer, date etc.
* Also set the direction as Forward or Reverse. 
* If the cycle sequencing plate contains reactions for both directions, then highlight the forward reaction wells, click on "Edit Selected Wells" and set the direction and primer. Do the same for the remaining reaction wells in the opposite direction.
* Add any additional comments in the Notes section, including which thermocycler was used, as well as the Full Plate Label field submitted in Signout. (This inlcudes the number Signout assigned to the plate when submitted for sequencing.)

Attaching Raw Traces to a Cycle Sequencing Plate
------------------------------------------------

To add a trace file to a single cycle sequencing reaction:

* Double click to open the reaction well of interest.  
* In the *Edit Wells* window that now appears, select the "Add/Edit Traces" button. 
* A new window will appear with an "Add Sequence(s)" button located in the upper left corner of the window. 
* Click the button and direct Geneious to the location of the raw trace file. Be sure to add only the correct trace (e.g. forward or reverse) to each reaction. 
* To remove one or more traces from a well, select the trace or traces in question and click "Remove Sequence(s)".


To bulk upload traces to a cycle sequencing plate or set of reactions:

* Open the appropriate cycle sequencing plate and click "Bulk Add Traces" on the plate’s toolbar. 
* Click "Browse" to point Geneious to the location of the trace files. Traces are matched to their corresponding cycle sequencing reactions based on components found in the trace file name (i.e., well number or field) along with name delimiters. For example, to attach a sample’s trace file to it’s corresponding well position based on the well position in the trace file name (for example, trace name 3726294 _\ **A01**\ _capture.ab1), the user would select the "Well number" button followed by "Match 2nd part of name", "separated by_(Underscore)" in the *Bulk add traces* dialog window.

.. figure:: /images/bulk_add_traces_well.png
  :align: center 

* To attach a sample’s trace file based on a field (in the above example, trace name **3726294**\ _A01_capture.ab1), the user would select the "Field" button followed by "Extraction Barcode" from the drop-down menu along with "Match 1st part of name, separated by _(Underscore)".

.. figure:: /images/bulk_add_traces_field.png
  :align: center 

* After all traces have been attached, click "OK" to create and save the cycle sequencing plate. 
* To double check that the traces have successfully attached the user can change the display options of the cycle sequencing plate so that # Traces is displayed. If the traces have attached correctly, wells should display "# Traces: 1".

.. figure:: /images/cycseq_display_number_traces.png
  :align: center 

* With the traces now attached to their corresponding cycle sequencing reaction plates, they are ready to be used by the Geneious Assembler. See :ref:`trace_download-link` instructions to begin the assembly process.
