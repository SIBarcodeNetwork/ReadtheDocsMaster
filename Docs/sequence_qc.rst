Quality control of assembled contigs
====================================

Go to the relevant folder in the local directory where the assembled bidirectional contigs are stored.
Select and open an assembly.

Manually editing assemblies
---------------------------

* Check the "Translation" option in the right hand menu of the Display window 

	* set the correct genetic code ("Vertebrate Mitochondrial" or "Invertebrate Mitochondrial" for COI, or "Bacterial" for rbcL and matK) and 
	* select the correct reading frame (black dots = stop codons, so we do not want any of these)

.. figure:: /images/assembly_view.png
  :align: center 	

* Quickly scan through the individual assemblies and assess whether or not each disagreement (if present) needs a manual edit.
* A manual edit ONLY needs to made if you feel the consensus sequences has been called incorrectly (or there is a gap that needs to be deleted). If Geneious calls the consensus sequence correctly, NO changes should be made to individual traces.
* If you are unhappy with the trimmed portions, you can edit these manually by clicking on, and dragging, the red bar indicating the trimmed region.

Checking sequence quality with alignments
-----------------------------------------

A second quality check is made by aligning your sequences based on the gene - align COI sequences together, rbcL together, etc. 

For alignments of protein coding regions Geneious's Translation Alignment program doesn't work like it should, so use an alternate program such an online program called TranslatorX (http://translatorx.co.uk) to create an alignment. 

.. note::
	It's important to note that TranslatorX only checks the forward reading frames, so you need to Reverse-Complement the matK sequences before putting them into this alignment program otherwise you will receive errors. 

* Export the consensus sequences (of good assemblies only) as a FASTA file then import this file into the program. We suggest you leave the Protein Alignment Option method selected as "Muscle". In the Genetic Code box select the relevant reading frame and be sure to check the "Guess most likely reading frame" option. Then hit Submit Query.
* If the program runs OK and doesn't encounter any errors, it will return an alignment of the nucleotides and also an alignment of the amino acids. You may download the fasta file of both, however, the alignment of amino acids is what will be used for the second quality check. Import the fasta file(s) of the alignments into Geneious for further analyses.
* Use the alignment to address any issue that you can see i.e. a clear difference between one sequence to the others (Remember this can be possible if the sequences are distantly related but still cross reference the alignment to the individual assemblies). Also, gaps must be assessed and resolved. Major differences in the alignment may also indicate that one or more of the sequences are contaminants (use BLAST to determine this).
* You may need to repeat the alignment step a number of times as you cross reference the assemblies and make edits. Save the edits, re-export all the consensus sequences and create a new alignment with these new consensus fasta files.
* If more than a handful of edits need to be made to the consensus sequence, the assembly should be discarded and the sample re-sequenced. You need to make a judgement call on this.
