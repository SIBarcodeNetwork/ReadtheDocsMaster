
Quality Control of Assembled Contigs
====================================

Here is an overview of the steps for sequence QC in Geneious. See below for more detailed information. 

1.	Note "failed" sequences
2.	Check primers have been removed for all remaining contigs 
3.	Set the correct genetic code
4.	Multiple alignments (There may be multiple iterations of this step)
5.	Trees
6.      BLAST


.. _qc_fails-link:

Failed Sequences
---------------- 

The easiest way to start the process of quality checking sequences is by marking which have failed. 

Traces that were not assembled due to low quality through the Geneious De Novo Assembler are considered fails. 

Assemblies that have less than 75% High Quality base calls (Geneious Prime field "% HQ") are also potential fails. As per the Barcode Data Standard, assemblies need to be 75% or over to be considered a high quality barcode sequence. However, the user may want to pursue further quality control on assemblies under 75% and not consider them failed based on importance of the sample.  

Traces and assembled contigs that are considered fails need to be noted in Geneious Prime. Based on user preference, notation can consist of color coding fails (right click on highlighted sequence files and choose "Set Document Color"), or dragging and dropping all fails into a unique folder within the local project Geneious Prime directory. The "Mark as Fail in LIMS..." Biocode Plugin tool should be used on failed sequences. See the :ref:`mark_pass-link` for instructions.


Manually Editing Assemblies
----------------------------

Continue the quality control process with the remaining assembled contigs.

Click into each assembly individually and scan through to assess whether or not each disagreement or ambiguity (if present) needs a manual edit. A manual edit ONLY needs to made if the user believes the consensus sequences has been called incorrectly based on the chromatogram peaks, or there is an unnecessary gap or base insertion that needs to be deleted. Sometimes it is not apparent that an edit is necessary for a protein coding sequence until the sequence has been translated (see below section). If Geneious Prime calls the consensus sequence correctly, **NO changes** should be made to base calls in individual traces within the assembly.
  
.. figure:: /images/manual_edit_ex1.png
  :align: center
  Example of a called base that can be corrected to avoid an ambiguity in the consensus
  
.. figure:: /images/manual_edit_ex2.png
  :align: center
  Example of a base deletion that can be corrected to avoid an ambiguity in the consensus

To manually edit an assembly, click the "Allow Editing" button in the toolbar of the "Contig View" tab (seen in above images) and proceed with the edit.

.. figure:: /images/manual_edit_dragtrim.png
  :align: center
  
Trimmed portions of traces can also be further edited manually by clicking on and dragging the pink bar indicating the trim annotation.

**Do not forget to save all edits.** This will be automatically prompted when clicking outside of the assembly document. Alternatively, click "Save" in the upper right corner of the "Contig View" tab toolbar.

.. figure:: /images/assembly_save_changes.png
  :align: center 

In addition, another window will prompt the application of changes the original sequences. **ALWAYS Click "Yes" to avoid losing connection to reference sequences.**

.. figure:: /images/assembly_apply_changes_to_originals.png
  :align: center 

 Genetic Code for Protein Coding Sequences
------------------------------------------

When looking at individual assemblies, check the "Translation" option in the right hand menu of the Display tab on the Geneious Prime Options Panel. 

.. figure:: /images/assembly_view2.png
  :align: center

Set the correct genetic code. This is typically "Vertebrate Mitochondrial" or "Invertebrate Mitochondrial" for COI, or "Bacterial" for rbcL and matK. For further information on NCBI genetic codes for a particular taxonomic group, see their `webpage <https://www.ncbi.nlm.nih.gov/Taxonomy/Utils/wprintgc.cgi>`_.

Select the correct reading frame. Black asterisks in the protein translation represent stop codons, and cannot be part of the open reading frame of a protein coding sequence (GenBank will not accept these).  If stop codons are present double-check the following:

		* the correct genetic code/reading frame is selected,
		* the assembly is in the correct orientation (Use "R.C." button in top left of the Contig View tab to to reverse complement the sequence and see if that helps),
		* whether insertions or deletions are present in the sequence that need to be edited, and/or
		* check BLAST to verify it is not a contaminant (see below for instruction)	
  
If BLAST indicates that the sequence is not a contaminant, persistant stop codons may be indicative of a **pseudogene** if the traces are high quality and there is no question of incorrect insertions or deletions in the sequence. Pseudogenes should still be submitted to GenBank, as they are valueable data, but proper annotation is necessary (see :ref:`noncoding_annotation-link` instructions).
  
Checking Sequence Quality with Alignments
-----------------------------------------

After needed edits have been made to individual assemblies, further quality control can be performed in Geneious Prime through alignments of consensus sequences. 

Analyzing the sequences' alignment will inform the user of any further end trimming needed if the Geneious Prime Assembler neglected to remove primers.

A sequence alignment is also a more efficient way to ensure that there are no stop codons in protein coding sequences, as the instructions in the above section can also be done with the sequence alignment document. 

Only align sequences that represent the same marker, i.e. align COI sequences together, rbcL together, etc. It may also be necessary to do multiple alignments of a single marker dataset if the organisms are phylogenetically distant. 

STEPS, including setting genetic code

REMOVE BELOW??

Geneious Prime's Translation Alignment program does not always correctly align protein coding sequences in highly variable regions (i.e. regions with homopolymers, etc.). To see a proper alignment in these cases, SIBN recommends the alternate program such an online program called TranslatorX (http://translatorx.co.uk) to create an alignment. 

.. note::
	It's important to note that TranslatorX only checks the forward reading frames, so it may be necessary to Reverse-Complement some sequences if errors are recieved when trying to run the alignment program. 

* Export the consensus sequences (of good assemblies only) as a FASTA file then import this file into the program. We suggest you leave the Protein Alignment Option method selected as "Muscle". In the Genetic Code box select the relevant reading frame and be sure to check the "Guess most likely reading frame" option. Then hit Submit Query.
* If the program runs OK and doesn't encounter any errors, it will return an alignment of the nucleotides and also an alignment of the amino acids. You may download the fasta file of both, however, the alignment of amino acids is what will be used for the second quality check. Import the fasta file(s) of the alignments into Geneious for further analyses.
* Use the alignment to address any issue that you can see i.e. a clear difference between one sequence to the others (Remember this can be possible if the sequences are distantly related but still cross reference the alignment to the individual assemblies). Also, gaps must be assessed and resolved. Major differences in the alignment may also indicate that one or more of the sequences are contaminants (use BLAST to determine this).
* You may need to repeat the alignment step a number of times as you cross reference the assemblies and make edits. Save the edits, re-export all the consensus sequences and create a new alignment with these new consensus fasta files.
* If more than a handful of edits need to be made to the consensus sequence, the assembly should be discarded and the sample re-sequenced. You need to make a judgement call on this.

Primer Removal
---------------------------

Geneious may miss some primers with the trim options we provided in the contig assembly step.

In the document table, sort all contigs by consensus length. The desired consensus length can vary depending on which sequencing primers were used but a general rule of thumb is that the COI-5P fragment is ~658 bp. For other barcode markers with less consistent length, use sequence alignments to ascertain if any consensus sequences extend past where the majority of other consensus sequences end. 

Trees
-----
Write this. NEW.

BLAST
-----

BLAST is a useful way to check the taxonomic ID of a questionable barcode sequence by comparing it to sequences in the NCBI nucleotide database. 

To BLAST the consensus of a single assembly, it is quickest to highlight and copy the consensus sequence from Geneious Prime and enter it into the online BLAST search page on the NCBI website (see http://blast.ncbi.nlm.nih.gov/Blast.cgi). 

Geneious Prime also provides the ability to BLAST a single or several sequences at a time from within the program itself, but is more time consuming. It is recommended to only BLAST small batches of 15 or less sequences when using this below method. To BLAST entire sequence datasets at once, see the (LINK to BLAST SOP) instructions to BLAST through the Biocode Plugin or within the Smithsonian High Compyting Cluster "Hydra".

To use BLAST small batches of assemblies, follow these directions:

* Select assemblies to be compared to the NCBI public DNA sequence database and click on the "BLAST" button in the Geneious Prime Toolbar.

.. figure:: /images/BLAST_button.png
  :align: center 

* The "BLAST" window appears and has multiple options for consensus, GenBank database, program etc. The selections in the image below are defaults, however, look into the various options and decide what works best for the user's dataset.

.. figure:: /images/BLAST_window.png
  :align: center

* The consensus options allows the user to choose how the program will call the consensus sequence of each assembly.

.. figure:: /images/BLAST_consensus_options.png
  :align: center

* Once selections have been made, click "Search" button in the "BLAST" window.
* The search progress appears in the Document Window. If this is too slow, there is a need to exit the search for whatever reason, click on the "Stop" button in the top left of the Document Window.
* Once complete, the results are saved in a subfolder (folder name ends with "- (nr_nt) blastn") within the folder containing the query sequence(s). If a batch search was done, there will be further subfolders containing BLAST results for each of the sequences.
* In the results folder the BLAST results are displayed in the "Hit Table" tab. Various information is included e.g. Hit Accession number, Query coverage, % Pairwise Identity, etc. Click on the manage columns icon found in the upper right of the table to choose what is displayed. Further information is found in the other tabs of the folder (Query Centric View, Annotations, Distances, Info).

.. figure:: /images/BLAST_hit_table.png
  :align: center

* To get more information about the individual BLAST hits, select one of the hits and the information about that sequence appears in the Document Viewer. Any of the columns can be sorted, rearranged, or resized.

