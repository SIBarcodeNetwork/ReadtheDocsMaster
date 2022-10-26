Cherry Picking
==============

Once the first round of sequence assembly and quality control is finished, and assembled contigs have been marked as Pass, Tentative, or Fail in the LIMS, some samples may need to be rerun through lab processes before project is considered complete. The process of selecting specific samples to be rerun is called "Cherry Picking".

Identify which samples will be cherry picked for reruns and plan how to organize these samples on new rerun plate(s). 

There are two options when cherry picking to build a rerun plate:

* Samples will either be aliquoted (subsampled) from the working stock plate or archive plate OR

* Entire tubes of sample DNA will pulled from the archive plate and moved to new plate. 

It is SIBN best practise that the rerun plate is build first in the lab, then in LIMS. Entering the plate data into LIMS after plate is built allows for correction of any error in planned well order that may occur while aliquoting or moving tubes. 

To create a rerun extraction plate (either aliquoted or phycially moved):

Follow instructions in the :ref:`create_ext_plate-link` instuctions until the point indicated.


.. _create_rerun-link:


Depending on whether aliquoting or moving tubes, follow the below instructions.

Aliquoting
----------

If taking aliquots for reruns, gather Extraction ID and Tissue Sample ID of rerun samples into a text list. Following the steps below will ensure that the original LIMS extraction plates are not altered. 

When creating the extraction plate, once at the *Edit Plate* window, paste in Tissue Sample IDs from text list to the corresponding wells in the **Tissue Sample ID** column.

Paste Extraction IDs into the **Parent Extraction ID** column, again making sure the well order is correct.

.. image:: /images/reruns_aliquoting.png
	:align: center
	:scale: 50 %

Click on the "Tools" button and select “Generate New Extraction IDs”.

When the new Extraction IDs have been generated, click "OK". 

FIMS data should now be associated with the wells in the rerun plate based on the Tissue Sample IDs. 

On the *New Extraction* window, click "OK" to save the aliquoted rerun plate.


Moving from Archive Plate
-------------------------

If physically moving the sample tubes from the archive plate to a new plate, the "Extraction Barcodes" stored in LIMS also need to be moved from the original extraction plates. 

For each rerun sample being physically moved, gather the original Extraction IDs only into a text file. 

Following the steps below will modify the original extraction plates in the LIMS, but will not break the link between the samples and workflows created thus far. 

When creating the extraction plate, once at the *Edit Plate* window, paste in Extraction IDs to the corresponding wells in the **Extraction ID** column. Click "OK". 

.. image:: /images/reruns_moving.png
	:align: center
	:scale: 50 %

This notice will appear: 

.. image:: /images/extractions_already_exist.png
	:align: center
	:scale: 50 %

Click the "Move extractions" button. 

Data from FIMS should now be associated with the wells in the rerun plate based on the Extraction ID and the Extraction Barcode should now also be moved to this plate.  

On the *New Extraction* window, click "OK" to save the rerun plate. 

If viewing the original extraction plate, wells that held samples now in the rerun plate should be empty.
