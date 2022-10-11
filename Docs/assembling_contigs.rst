Assembling Contigs
==================

Once traces have been downloaded and organized within the user's local Geneious directories, the raw data needs to be assembled into bidirectional contigs. The Geneious Assembler Module is used to edit, save, export and ultimately publish the data. 

**Hereafter, these bidirectional contigs will be referred to interchangably as either "contigs" or "assemblies".**

Two slightly different pipelines can be employed for trimming the raw traces and assembling them into contigs:

1. Incorporating the trimming of traces into the assembly function
2. Trimming all traces first, then assembling into contigs

.. note::
	Any settings or parameter values outlined below are guidelines. It is recommended that the user evaluates different trim and assembly settings to establish what is optimal for the group and/or marker being analyzed.

OPTION 1: Trimming and Assembling at the Same Time
--------------------------------------------------

* Select all the raw traces to be assembled into a contig.
* Click on "Align/Assemble" in the toolbar.
* Select "De Novo Assemble" in the dropdown menu. 

.. figure:: /images/align_assemble_denovo.png
  :align: center

*De Novo Assemble* Window
~~~~~~~~~~~~~~~~~~~~~~~

* In the "Data" section, specify the unique part of the trace filename to be used to match the forward and reverse direction traces. This will depend on how raw traces are labelled. 
* In the "Method" section, choose the Assembler and Sensitivity. The options displayed below are recommended, however, it is also possible to choose "Custom Sensitivity" from the dropdown menu, and choose custom parameters (for example, minimum overlap). When "Custom Sensitivity" is selected, many of the options in the "Advanced" section of the window will become available.
* In the "Results" section, insert an Assembly Name, or leave as the default. After the assembly is complete all contigs will be deposited in a folder in the local directory with this title. "Save assembly report" and "Save results in a new subfolder" should both be selected. 
* In the "Advanced" section, ensure that the "Circularize contigs with matching ends" option is unchecked.
* In the "Trim Sequences" section select "Trim Sequences" and then click on the Option button. A *Trim Options* window should appear.

.. figure:: /images/de_novo_assemble.png
  :align: center 

*Trim Options* Window
~~~~~~~~~~~~~~~~~~~

When creating sequencing assemblies, be sure to select the correct options in the *Trim Options* window.

.. figure:: /images/trim_options.png
  :align: center 

The first option to choose between is "Annotate new trimmed regions" or "Remove trimmed regions from sequences". If "Annotate new trimmed regions" is selected, then the information in the trimmed region of the trace is annotated and not deleted. The underlying raw data is maintained throughout downstream analyses for possible adjustment later in the pipeline. Assembly and other analyses automatically take the trims into account, and exclude these regions in all calculations. 

If either "Remove new trimmed regions from sequences" or "Remove existing trimmed regions from sequences" is selected (the latter option will only show in this window when the selected traces have been previously trimmed), then the trimmed regions are deleted and the associated information will not be available for downstream analyses.

"Trim vectors" uses a clone of NCBI's VecScreen tool (Altschul et al, 1997) to screen for vector contaminants from the NCBI UniVec database. 

Check "Trim Primers" to trim the appropriate PCR primers from each raw trace. Clicking the "Choose" button opens the *Select Primers* window. This window should open to the user's list of primers that are saved in local directory. It is possible to choose as many primers for trimming as required. 

* If using M13 tagged PCR primers, make sure both M13 and untagged primer documents are saved locally. Just select the untagged version of the primer for trimming, since the chance of finding the longer tagged version of the primer is slimmer than finding the untagged version.
* Select the "Allow Mismatches" option and list "2" - if too high a number is listed here it will "find" the primers at the incorrect locations of the read.
* For a primer of 15-20 bp in length, select "10" for Minimum Match Length. If too low a number is selected too here it will "find" the primers at incorrect locations of the read.

"Error Probability Limit" value of 0.05 is an appropriate starting value for trimming. This option works by trimming the trace sequence to find the longest possible untrimmed region, which has an overall error probability less than 5%. To trim more aggressively, decrease the limit or manually edit the trim by clicking and dragging either end of the annotation in the Sequence View.

* Select both Trim 5' End and Trim 3' End options, but leave "At least" UNCHECKED.
* Leave "Maximum length after trim" UNCHECKED.
* Once all settings are complete hit "OK". Back in the *De Novo Assemble* window, click "OK" to begin the trim/assembly process. All the assemblies and an Assembly Report will be deposited into the subfolder that was specified/named in the local directory. Geneious will generate a new subfolder each time a De Novo Assembly is run.


OPTION 2:Trimming and Assembling in Two Separate Steps
------------------------------------------------------

To trim traces:

* Highlight all relevant traces in the Document Table.
* Select "Annotate & Predict" from the Menu bar.
* Choose "Trim Ends" from the drop-down menu. 

.. figure:: /images/annotate_predict_trim_ends.png
  :align: center

A *Trim Ends* window will open and this is essentially the same as the *Trim Options* window described earlier. Proceed with directions as laid out for that window.

To assemble previously trimmed raw traces into a contig:

* Select all of the traces to assemble (and a reference sequence or list if applicable) then click the "Align/Assemble" drop-down button in the Toolbar. 
* Select "De Novo Assemble". 
* The *De Novo Assemble* window opens. See previous section for description of the options available in this window. The only difference is noted below.
* Since the trace sequences were previously trimmed, select "Use existing trim regions" in the "Trim Before Assembly" part of the window. 

Assembly Report
-----------------
The assembly report is found in the assemblies folder, regardless of implementing Option 1 or Option 2. It provides a record of which traces were assembled successfully and which traces failed. The blue hyperlink next to the green checkmark at the top of the report links to all traces that assembled successfully. The blue hyperlink next to the red "X" points the user to all traces that failed to assemble. Click the hyperlink to highlight all trace files that were not assembled. See the :ref:`qc_fails-link` instructions to handle failed traces.

.. figure:: /images/assembly_report.png
  :align: center 
  

Additional Information
----------------------

It is possible to re-trim trace sequences using different parameters at any stage. To do so select the traces for re-trimming and follow the steps outlined above. The only difference is the "Annotate new trimmed regions" option should be selected to have the new trims replace the old trims. When a trace sequence is re-trimmed, it stores the history of trims in the "Info" tab for each trace.

Manually trimming traces is also an option. To manually trim a trace, select a region at the end of the trace in the Sequence View, click "Add Annotation".

.. figure:: /images/add_annotation_trimmed1.png
  :align: center

On the *Add Annotation* window, choose "Trimmed" for the annotation type and click "OK". Trimmed annotation should be applied to the highlighted region of the trace. 

.. figure:: /images/add_annotation_trimmed2.png
  :align: center

If a trace has multiple trimmed annotations for the same region, the largest trimmed annotation will be used.

