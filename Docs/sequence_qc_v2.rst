Quality Control of Assembled Contigs
====================================

Here is an overview of the steps for sequence QC in Geneious. See below for more detailed information. 

1.	Create a "fails" folder and move all obvious fails to this folder
2.	Check primers have been removed for all remaining contigs 
3.	Set the correct genetic code
4.	Multiple alignments (There may be multiple iterations of this step)
5.	Trees
6.      BLAST

Go to the relevant folder in the local directory where the assembled bidirectional contigs are stored.
Select and open an assembly. The below steps can be done in any order as per user preference.

Obvious Fails
---------------------------
Highlight red (or color preferred by user) and mark as fail


Manually Editing Assemblies
----------------------------
Removing ambiguities and bringing "% Pairwise identity" to 100% where able

.. figure:: /images/assembly_view.png
  :align: center 
  
* Quickly scan through the individual assemblies and assess whether or not each disagreement (if present) needs a manual edit.
* A manual edit ONLY needs to made if you feel the consensus sequences has been called incorrectly (or there is a gap that needs to be deleted). If Geneious calls the consensus sequence correctly, NO changes should be made to individual traces.
* To manually edit an assembly, the "Allow Editing" button in the toolbar of the contig window should be clicked on (see image above). 
* If you are unhappy with the trimmed portions, you can edit these manually by clicking on, and dragging, the red bar indicating the trimmed region.
* **Do not forget to save your edits.** You will be prompted to do this when you try to close the assembly. 

.. figure:: /images/assembly_save_changes.png
  :align: center 

* In addition, another prompt window will ask if you want to apply changes to the original sequences. **ALWAYS Click "Yes", because you risk losing connection to reference sequences.**

.. figure:: /images/assembly_apply_changes_to_originals.png
  :align: center 

Primer Removal
---------------------------

Geneious may miss some primers with the trim options we provided in the contig assembly step.

In the document table, sort all contigs by consensus length. The desired consensus length can vary depending on which sequencing primers were used but a general rule of thumb is that the COI-5P fragment is ~658 bp. For other barcode markers with less consistent length, use sequence alignments to ascertain if any consensus sequences extend past where the majority of other consensus sequences end. 


Checking Sequence Quality with Alignments
-----------------------------------------

A second quality check is made by aligning sequences based on the gene - align COI sequences together, rbcL together, etc. This may be done in Geneious Prime.

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

Genetic Code
---------------------------
* **If you are editing protein coding genes**, check the "Translation" option in the right hand menu of the Display window 

	* Set the correct genetic code ("Vertebrate Mitochondrial" or "Invertebrate Mitochondrial" for COI, or "Bacterial" for rbcL and matK) and 
	* Select the correct reading frame. Black dots = stop codons, so we do not want any of these. If stop codons are present double-check the following:

		* the correct genetic code is selected,
		* the assembly is in the correct orientation (Use "R.C." button in top left of contig window if you need to reverse complement it),
		* whether insertions or deletions are present that need to be edited, and/or
		* check BLAST to verify it is not a contaminant (see below for instruction)	



Trees
-----
Write this. NEW.

BLAST
-----

BLAST is a useful way to check the taxonomic ID of a questionable barcode sequence by comparing it to sequences in the NCBI nucleotide database. 

To BLAST the consensus of a single assembly, it is quickest to highlight and copy the consensus sequence from Geneious Prime and enter it into the online BLAST search page on the NCBI website (see http://blast.ncbi.nlm.nih.gov/Blast.cgi). 

Geneious Prime also provides the ability to BLAST several sequences at a time from within the program itself. It is recommended to only BLAST small batches of 15 or less sequences when using this below method. To BLAST entire sequence datasets, see the (LINK to BLAST SOP) instructions to BLAST through the Biocode Plugin or within the Smithsonian High Compyting Cluster "Hydra".

To use BLAST small batches of assemblies, follow these directions:

* Select assemblies to be compared to the NCBI public DNA sequence database and click on the "BLAST" button in the Geneious Prime Toolbar.

.. figure:: /images/BLAST_button.png
  :align: center 

* The "BLAST" window appears and has multiple options for consensus, GenBank database, program etc. The selections in the image below are SIBN recommendations for querying COI sequences, however look into the various options and decide what works best for the user's dataset.

.. figure:: /images/BLAST_window.png
  :align: center

* The consensus options allows you to choose how the program will call the consensus sequence of each assembly.

.. figure:: /images/BLAST_consensus_options.png
  :align: center

* Once you have made your selections, click "Search" button in the "BLAST" window.
* The search progress appears in the Document Window. If this is too slow, or you want to exit the search for whatever reason, click on the "Stop" button in the top left of the Document Window.
* Once complete, the results are saved in a subfolder (folder name ends with "- nr Megablast") within the folder containing your query sequence(s). If you did a batch search, there will be further subfolders containing BLAST results for each of the sequences you entered into the BLAST search.
* In the results folder the BLAST results are displayed in the "Hit Table" tab. Various information is included e.g. Hit Accession number, Query coverage, % Pairwise Identity, etc. You can choose what is displayed by clicking on the manage columns icon found in the upper right of the table. Further information is found in the other tabs of the folder (Query Centric View, Annotations, Distances, Info).

.. figure:: /images/BLAST_hit_table.png
  :align: center

* To get more information about the individual BLAST hits, select one of the hits and the information about that sequence appears in the Document Viewer. Any of the columns can be sorted, rearranged, or resized.

