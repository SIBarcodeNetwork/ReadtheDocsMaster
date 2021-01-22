Updating Existing GenBank Records
=================================

Now that your records have been published in GenBank, you may notice that there are fields that need to be added or updated.

Who has permission to update a GenBank record?
----------------------------------------------

Only individuals listed as sequence authors can submit an update. If an update is requested by someone not listed as an author, you must "cc" one of the authors in your email, and request that author give authorization for the update. You may also want to request that the sequence author add you as another sequence author to the Genbank records that require updating.

Updating a single GenBank record
--------------------------------

To update a single GenBank record, you can usually just include all updated information directly in email text. For example, if you want to update the scientific name identification for an existing record ABC123, just send an email to gb-admin@ncbi.nlm.nih.gov with the following text:

  Can you please update the "organism" field of GenBank record ABC123 ([*adding a link is helpful*]) to "Genus species"?

You can even update nucleotide sequences in this way -- no need to attach a FASTA file for just a single GenBank record update.

Updating several GenBank records
--------------------------------

In order to update several GenBank records at once, you will need to prepare 1 or more files. For further details on how to submit sequence record updates to Genbank, see their page `Updating Information on Genbank Records <https://www.ncbi.nlm.nih.gov/genbank/update/>`_. 
The 3 most common types of updates to barcode records will be:

  * Source information (any of the modifiers in the "source" section of the record)
  * Nucleotide sequence
  * Publication information (any of the data in the "references" section of the record) 

Source information
~~~~~~~~~~~~~~~~~~

The GenBank "source modifiers" are any of the fields in a GenBank record that pertain to the Specimen metadata portion of the Barcode Data Standard. To make a change to one or more of these fields, you will need to prepare a spreadsheet table with Accession in the first column, and all of the fields you want to change in the subsequent columns.

Coming Soon: Add instructions for using genetic_collections to download a source table to start with.

Save the spreadsheet as a tab-separated text file (.tsv), and attach to an email to gb-admin@ncbi.nlm.nih.gov with the following text:
  
  Can you please update the [*fields you would like to change*] fields for the GenBank accessions in the attached file [*filename*]?
  
Also, if you wanted to add any sort of custom note to your sequence records, such as one regarding the confidence level of the taxonomic IDs, you would use the "Note" Genbank source modifier as a field in your .tsv table. Because you are adding a field to your records, rather than updating an existing one, alter the email request as follows:  

  Can you please add the [*fields you would like to add*] fields to the GenBank accessions in the attached file [*filename*]?
  
Nucleotide sequences
~~~~~~~~~~~~~~~~~~~~

To update nucleotide sequences for multiple Genbank records, you will have to gather the sequences to be updated in single FASTA file, each named by their Genbank Accession. If your sequences are in Geneious Prime, you may have to rename each sequence to their Genbank Accession number by hand, as that information will not be in the FIMS or LIMS. To do this, simply double click (slowly) on the current sequence name and you should be able to edit it. To download sequences in a FASTA file from the Geneious Prime go to File>Export>Documents>FASTA sequences/alignment. 

Email this file to gb-admin@ncbi.nlm.nih.gov, with the following text:
  
  Can you please update the nucleotide sequences for the GenBank accessions in the attached file [*filename*]?

Publication information
~~~~~~~~~~~~~~~~~~~~~~

If you have a single publication to add to a range of Genbank accessions, simply list the full citation of the publication along with the range of accessions in the text of an email request to gb-admin@ncbi.nlm.nih.gov, for example:
  
  Can you please add the publication reference [*full citation*] to the GenBank accessions [*accession range*]?

From the full citation, Genbank staff will be able to pull Author, Title, Journal, etc. information for the fields in the record.

Similarly, if you have Sequence Authors (can be more than one) to add universally to a range of Genbank accessions, you can request this addition in the text of an email. 

  Can you please add [*first_initial middle_initial surname*] as a Sequence Author to the GenBank accessions [*accession range*]?
  
Again, if you are submitting a request and are not already listed as a Sequence Author, Genbank staff will need to see approval from an existing Sequence Author, and you should request that your name be included in the Sequence Author list. 

Note: At least one author must be shared between Sequence Authors and Publication Authors on the Genbank record. If Sequence Authors were not included as authors in the publication, you will need to request the addition of a publication author to the list of Sequence Authors.

Adding multiple publications and author information to sequence records should be similar to adding/editing Source Modifier information, as you will gather fields to be added into a .tsv table file and email to gb-admin@ncbi.nlm.nih.gov, requesting that they add the publication and authorship information to a specific range of accessions specified in the attached file. For potential publication and authorship fields to add, see https://www.ncbi.nlm.nih.gov/genbank/update/#pub

 


