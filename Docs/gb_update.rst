Updating Existing GenBank Records
=================================

Now that your records have been published in GenBank, you may notice that there are fields that need to be added or updated.

Who has permission to update a GenBank record?
----------------------------------------------

Anyone listed as a sequence author can submit an update. In addition, if an organization is listed in the "Consortium" field of a record, then anyone associated with that organization can submit an update. It is preferable for an update to come directly from one of these people, but you can also include the author(s) in the update email via "cc".

Updating a single GenBank record
--------------------------------

To update a single GenBank record, you can usually just include all updated information directly in the email text. For example, if you want to update the scientific name identification for an existing record ABC123, just send an email to gb-admin@ncbi.nlm.nih.gov with the following text:

  Can you please update the "organism" field of GenBank record ABC123 ([*adding a link is helpful*]) to "Genus species"?

You can even update nucleotide sequences in this way -- no need to attach a FASTA file for just a single GenBank record update.

Updating several GenBank records
--------------------------------

In order to update several GenBank records at once, you will need to prepare 1 or more files. The 3 most common types of updates to barcode records will be:

  * Source information (any of the modifiers in the "source" section of the record)
  * Nucleotide sequence
  * Publication information (any of the data in the "references" section of the record)

Source information
~~~~~~~~~~~~~~~~~~

The GenBank "source modifiers" are any of the fields in a GenBank record that pertain to the Specimen metadata portion of the Barcode Data Standard. To make a change to one or more of these fields, you will need to prepare a spreadsheet table with Accession in the first column, and all of the fields you want to change in the subsequent columns.

TO DO: Add instructions for using genetic_collections to download a source table to start with.

Save the spreadsheet as a tab-separated text file (.tsv), and attach to an email to gb-admin@ncbi.nlm.nih.gov with the following text:
  
  Can you please update the [*fields you would like to change*] fields for the GenBank accessions in the attached file [*filename*]?

Nucleotide sequences
~~~~~~~~~~~~~~~~~~~~

TO DO: Add instructions on how to create and email FASTA file to update multiple sequence records.

Publication information
~~~~~~~~~~~~~~~~~~~~~~

TO DO: Add instructions on how to email publication information changes -- specifically how to request addition of Consortium and/or Sequence Authors, so that changes can be made more flexibly in the future. 


