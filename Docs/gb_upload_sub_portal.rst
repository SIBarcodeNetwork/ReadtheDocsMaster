GenBank Upload Pipeline 1: GenBank Submission Portal
=====================================================

The GenBank Submission Portal on the NCBI website must be used to submit metazoan (multicellular) mtCOI and/or any rRNA sequences (such as 18S, 16S, 23S, 28S, ITS, etc.), as GenBank no longer supports submissions of these markers through the Geneious Prime GenBank Submission plug-in. This plug-in can still  be used to submit all other markers (See GenBank Upload Pipeline 2 (LINK ONCE COMPLETE) for a detailed step by step of how to use the plug-in).  

To demonstrate GenBank submission via the Submission Portal , a batch of ITS fungal barcodes will be used as an example. 

Navigate to the NCBI Submission Portal: https://submit.ncbi.nlm.nih.gov/ 

Click on “Log in” in the upper right corner.  NCBI now uses third party accounts to sign in, so either a Google or an SI.gov username and password should work.

.. figure:: /images/ncbi_submission_portal_sign_in.png
 :align: center
 :target: /en/latest/_images/ncbi_submission_portal_sign_in.png

Back on the Submission Portal page, in the search box, type “GenBank” and the link to the GenBank submission tool will appear as one of the suggested options. filename: ncbi_submission_portal_genbank.png

On the first page of the GenBank submission process, it is possible to click through the headings on the left of the “What You Should Expect” section to learn more about the requirements. 

.. figure:: /images/ncbi_submission_Genbank_tool.png
 :align: center
 :target: /en/latest/_images/ncbi_submission_Genbank_tool.png
 
When ready to continue, click the “Submit” button.

Click the “New submission” button.

.. figure:: /images/ncbi_submission_portal_GB_new_submission.png
 :align: center
 :target: /en/latest/_images/ncbi_submission_portal_GB_new_submission.png

This will lead to a series of 8 tabs where data will be filled in or uploaded. If there is organism information that is new to NCBI, an extra “Organism” tab will appear later on. The tabs are detailed below.

1. Submission Type Tab:
---------------------

.. figure:: /images/gb_subportal_submission_type.png
 :align: center
 :target: /en/latest/_images/gb_subportal_submission_type.png

Choose the region to be submitted and specify any further details as necessary. Specifying a “Submission title” can be useful for organizing submissions within one’s NCBI account. Click “Continue”.

2. Submitter Tab:
---------------------

.. figure:: /images/gb_subportal_submitter.png
 :align: center
 :target: /en/latest/_images/gb_subportal_submitter.png

Fill in the submitter’s affiliated institution and contact information. Click “Continue”.

3. Sequencing Technology Tab:
---------------------

.. figure:: /images/gb_subportal_seqtech.png
 :align: center
 :target: /en/latest/_images/gb_subportal_seqtech.png
 
Indicate the technology used to obtain sequences and whether sequences are assembled or unassembled. 

4. Sequences Tab: 
---------------------

.. figure:: /images/gb_subportal_sequences.png
 :align: center
 :target: /en/latest/_images/gb_subportal_sequences.png

Indicate when sequences should be released. SIBN funded projects require that sequences be released as soon as possible and no later than 12 months of sequence generation. Please see :ref:`rapid_data_release-link` page for more information and contact SIBN staff if you have questions about this requirement.

Sequences need to be uploaded in a FASTA file. Sequences can be exported in this format from Geneious Prime using the :ref:`Exporting_fasta-link` instructions.

Before exporting from Geneious Prime, ensure that local Geneious files have been renamed by the voucherCatalogNumber (the DwC triplet or doublet from GeOMe FIMS) using the :ref:`Batch_rename-link` instructions. 
  
  Note: This assumes that voucher numbers represented by voucherCatalogNumber are unique across the sequences to be submitted. If this is not the case, another unique value such as tissueBarcode may be used to name sequences with the Batch Rename function.
    
Once the FASTA file has been exported from Geneious Prime, follow the instructions on the GenBank Submission Portal to upload. Click “Continue”.

The Submission Portal now processes and validates the uploaded sequences to ensure the correct sequence type has been selected and that there are no stop codons, if submitting COI. If any sequences are flagged, the Portal will create a downloadable report identifying problematic sequences. These need to be fixed before proceeding.
