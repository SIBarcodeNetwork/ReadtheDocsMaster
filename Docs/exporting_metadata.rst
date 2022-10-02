.. _Exporting_metadata-link:

Exporting Sequence Metadata in TSV format
==========================================

In Geneious Prime, gather all assemblies or consensus sequences from which metadata will be exported into a local folder.

Make sure the most up-to-date FIMS and LIMS metadata are associated with the sequences. To do this, follow the instructions on the :ref:`Annotating_FIMS_LIMS-link` page to annotate the sequence files with the current GeOMe FIMS and Biocode LIMS data. 

To export sequence metadata, first select all relevant files.

Export the sequence metadata by using the Export function in the Geneious Prime Toolbar and choosing “Export Documents”. 

.. image:: /images/geneious_export_documents.png
  :align: center
  :target: /en/latest/_images/geneious_export_documents.png

A *Select Format* window will open, but will contain different options dependent on whether export is from consensus sequence or assembly files.

.. figure:: /images/geneious_tsv_export_consensus.png
  :align: center
  :target: /en/latest/_images/geneious_tsv_export_consensus.png 
   
  The *Select Format* window when exporting from consensus sequence files

.. figure:: /images/geneious_tsv_export_assembly.png
  :align: center
  :target: /en/latest/_images/ggeneious_tsv_export_assembly.png
   
  The *Select Format* window when exporting from assembly files

In either case, select “TSV tab-separated table (*.tsv)”.

Next, name the fasta file, select the local directory in which to save it, and click “Proceed” on the *Potential Data Loss* window.

.. image:: /images/geneious_PotentialDataLoss_tsv.png
  :align: center
  :target: /en/latest/_images/geneious_PotentialDataLoss_tsv.png

A list of FIMS and LIMS column headers should then appear. FIMS column headers start with a lowercase letter, and LIMS column headers start with an uppercase letter.

.. figure:: /images/geneious_column_headers_assembly.png
  :align: center
  :target: /en/latest/_images/geneious_column_headers_assembly.png
  
  *TSV tab-separated Export* window that appears when exporting from assembly files

If exporting from assembly files, at the top of the window, ensure that “Documents” is selected. This will not be necessary if exporting from consensus sequence files. 

From this list, choose all fields that are needed, then click “OK”. The tsv file will be exported to the location previously specified.
