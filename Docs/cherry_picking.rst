Cherry Picking
==================================

After you’ve finished your sequence QC and marked your assemblies as Pass or Fail in the LIMS, you may need to perform additional lab work to finish off your project. You will need to decide which samples will be included in your rerun plates and how you plan to organize these samples in a new plate or plates. You will probably choose to either aliquot from your working stock into a new plate, or go back to your archive plate and pull out the samples that need to be rerun. 

Aliquoting
------------------

If you’ve decided the best plan of action is making aliquots from your working stock, you’ll want to create the rerun plate in the lab, and then create it in the LIMS as well. You’ll need the Extraction IDs and Tissue Sample IDs from the samples you are including for this process. Following the steps below will ensure that your original extraction plates are not modified in the LIMS. 

To create a new plate of aliquots in the LIMS:
* Click the “New Reaction” button on the Geneious toolbar, just as if you were creating a new extraction plate. 
* In the “New Reaction” window, make sure the Type of reaction is set to “Extraction”, and that “96 well plate” is ticked. Click OK.
* A new window will open showing an empty plate map. You will want to give your plate a name. Make sure to follow the guidance in :ref:`lims_conventions-link` for a rerun plate.
* Click the Bulk Edit button to enter the sample information that will link this plate to the FIMS/LIMS data already entered. 
* In the Edit Plate window that opens, paste in your Tissue Sample IDs to the corresponding wells. 
* Paste your Extraction IDs into the Parent Extraction ID column, again making sure the well order is correct. 
* Click on the Tools button and select “Generate New Extraction IDs”. At this point, your window should look like this: 

.. image:: /images/reruns_aliquoting.png
	:align: center
	:scale: 50 %

* When the new Extraction IDs have been generated, click OK. 

You should now see that the data from your FIMS is included in the plate you have created. Don’t forget to save the plate. 

Moving the samples
------------------

If you’ve decided to physically move the samples in the matrix plates, you’ll need to move them from the extraction plates you created in the LIMS as well. You’ll need the Extraction IDs of the original samples for this process. Following the steps below will modify your original extraction plates in the LIMS, but it should not break the link between the samples and all the work you have done on them thus far. 

To move the samples to a new extraction plate in the LIMS:
* Click the “New Reaction” button on the Geneious toolbar, just as if you were creating a new extraction plate. 
* In the “New Reaction” window, make sure the Type of reaction is set to “Extraction”, and that “96 well plate” is ticked. Click OK.
* A new window will open showing an empty plate map. You will want to give your plate a name. Make sure to follow the guidance in :ref:`lims_conventions-link` for a rerun plate.
* Click the Bulk Edit button to enter the sample information that will link this plate to the FIMS/LIMS data already entered. 
* In the Edit Plate window that opens, paste in your Extraction IDs to the corresponding wells. Click OK. 

.. image:: /images/reruns_moving.png
	:align: center
	:scale: 50 %

* At this point you should see the error screen below: 

.. image:: /images/extractions_already_exist.png
	:align: center
	:scale: 50 %

* Click the Move extractions button. 

You should now see that the data from your FIMS is included in the plate you have created. Don’t forget to save the plate. 
