Updating Existing GenBank Records
=================================

Once records have been published in GenBank, there may be fields that need to be added or updated.

Who has Permission to Update a GenBank Record?
----------------------------------------------

Only individuals listed as **sequence authors** can submit an update. If an update is requested by someone not listed as an author, that individual must "cc" one of the authors in the email, and request that author give authorization for the update. The person requesting the update may also want to request to be added as a sequence author themselves.

Updating a Single GenBank Record
--------------------------------

To update a single GenBank record, just include all updated information directly in email text. For example, to update the scientific name identification for an existing record AB123456, just send an email to gb-admin@ncbi.nlm.nih.gov with the following text:

  Can you please update the "organism" field of GenBank record AB123456 ([*adding a link is helpful*]) to "Genus species"?

Nucleotide sequences can also be updated in this way -- no need to attach a FASTA file for just a single GenBank record update. 

Publication information additions or updates to a single record can be done this way as well.

Updating Several GenBank Records
--------------------------------

In order to update several GenBank records at once, 1 or more files need to be prepared. For further details on how to submit sequence record updates to GenBank, see their page `Updating Information on GenBank Records <https://www.ncbi.nlm.nih.gov/genbank/update/>`_. 
The 3 most common types of updates to barcode records will be:

  * Source information (any of the modifiers in the "source" section of the record, including "organism", "specimen_voucher", etc.)
  * Nucleotide sequence
  * Publication information (any of the data in the "reference" sections of the record) 

Source Information
~~~~~~~~~~~~~~~~~~

The GenBank "source modifiers" are any of the fields in a GenBank record that pertain to the specimen metadata portion of the Barcode Data Standard. To make a change to one or more of these fields, prepare a spreadsheet table with "acc. num." (GenBank accession number) in the first column, and all of the fields to be changed or added in the subsequent columns.

Save the spreadsheet as a tab-separated text file (.tsv), and attach to an email to gb-admin@ncbi.nlm.nih.gov with the following text:
  
  Can you please update(or add) the [*fields to be changed/added*] fields for the GenBank accessions in the attached file [*filename*]?
  
Nucleotide Sequences
~~~~~~~~~~~~~~~~~~~~

To update nucleotide sequences for multiple GenBank records, gather the sequences to be updated in single FASTA file, each named by their GenBank Accession. If the corrected sequences are in Geneious Prime, it is possible that each may need to be renamed with the GenBank accession number by hand, as there is not a straitforward way to backfill GB accessions into LIMS or FIMS at this time. To do this, simply double click (slowly) on the current sequence name to edit. To then download sequences in a FASTA file from the Geneious Prime see the :ref:`Exporting_fasta-link` instructions. 

Email this file to gb-admin@ncbi.nlm.nih.gov, with the following text:
  
  Can you please update the nucleotide sequences for the GenBank accessions in the attached file [*filename*]?

Publication Information
~~~~~~~~~~~~~~~~~~~~~~

If a single publication needs to be added to a range of GenBank accessions, simply list the full citation of the publication along with the range of accessions in the text of an email request to gb-admin@ncbi.nlm.nih.gov, for example:
  
  Can you please add the publication reference [*full citation*] to the GenBank accessions [*accession range*]?

From the full citation, GenBank staff will be able to pull Author, Title, Journal, etc. information for the fields in the record.

Similarly, if Sequence Authors (can be more than one) need to be added universally to a range of GenBank accessions, request this addition in the text of an email. 

  Can you please add [*first_initial middle_initial surname*] as a Sequence Author to the GenBank accessions [*accession range*]?
  
Again, if an individual is submitting a request and is not already listed as a Sequence Author, GenBank staff will need to see approval from an existing Sequence Author, and the individual should be added to the Sequence Author list. 

.. note::

   At least one author must be shared between Sequence Authors and Publication Authors on the GenBank record. If Sequence Authors were not included as authors in the publication, request the addition of a Publication Author to the list of Sequence Authors.

Adding multiple publications and author information to sequence records should be similar to adding/editing Source Modifier information, fields need to be listed in a .tsv table file and emailed to gb-admin@ncbi.nlm.nih.gov, requesting that they add the publication and authorship information to a specific range of accessions specified in the attached file. For potential publication and authorship fields to add, see https://www.ncbi.nlm.nih.gov/genbank/update/#pub.

 


