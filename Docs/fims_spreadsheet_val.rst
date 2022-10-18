FIMS Validation and Upload
======================================

Once a spreadsheet is fully populated, it must be validated and *possibly* uploaded to the GEOME FIMS database. The validation step checks every specimen record to make sure that they meet the set of rules established by the project. 

If SIBN is performing the lab work for a project, only work through the “Validation without Loading” section below and then email the spreadsheet to the SIBN project manager, who will complete the upload of data to the GEOME FIMS. 

Validation without Loading
---------------------------

Go to https://geome-db.org/ and click on Workbench. 

From the list of public projects, click on "SI Barcoding Network (SIBN)".

If not logged in, click "Validate Data" from the menu on the left.

Or, if already logged into GEOME, click "Load Data" from the menu on the left, and then tick the “Only validate data” box at the top of the Load Data screen.

Where it says ‘Excel Workbook’, click the Browse button to select the appropriate spreadsheet. 

Select the pre-existing expedition called “_SIBN_Validation” and click the Validate button.

If the spreadsheet does not pass validation, specific issues should be listed. Resolve the issues and try validating again. If the spreadsheet passes validation, forward it on to the SIBN project manager.

*Note: To pass validation, data must be in a tab named "Samples" within the spreadsheet.*

.. image:: /images/fims_validation.png
  :align: center
  :target: /en/latest/_images/fims_validation.png

Validation and Loading
-----------------------

Go to https://geome-db.org/, click on the user profile image with the down-pointing caret at the top, and then click on Sign in.

Log in with GEOME username and password. While logging into GEOME is not required for validation, it is required for uploading data. 

After logging in, go to Workbench and then click Load Data from the menu on the left. 

.. image:: /images/fims_validation_upload.png
  :align: center
  :target: /en/latest/_images/fims_validation_upload.png

Where it says ‘Excel Workbook’, click the Browse button to select the appropriate spreadsheet. 
	
If the samples being uploaded are not part of an existing expedition within GEOME, a new one needs to be created. In the Expedition Name drop-down that appears, click the plus sign to the right of the box and enter the SIBN project name. (The same name should go in Expedition Title and Expedition Code.) Remember to follow the :ref:`conventions-link`, and make sure not to repeat a previously created expedition code.

.. note::

   While the expedition title can be modified at any time, the expedition code is a unique identifier and cannot be changed.

If adding to or updating data previously uploaded, simply select the associated project from the Expedition Name drop-down. 

	If adding new samples to an existing GEOME expedition, only the new samples need to be in the spreadsheet to be uploaded.

	**Only click “Replace expedition data”** if samples from previously uploaded data need to be deleted from GEOME. Ensure all data from the expedition has been downloaded as a copy **before** replacing it with new data.

If ready to upload the spreadsheet, click the Load button. If there are no errors, the screen should return a “Successfully Validated!” message.


Double Checking the Upload
--------------------------

To double check that the upload was successful, click on the Query button at the top of the screen.

	On the Query page, data can be viewed from any expedition in any of the individual projects (e.g. SI Barcoding Network, BOEM, SI Bioblitz, etc.) in the GEOME FIMS. This is why it is important not to include sensitive information (e.g. highly accurate GPS coordinates for protected species) in spreadsheet uploads. 

To see the expedition that was just uploaded, first click on “Switch to Advanced Search” in the top right of the search screen. 

Then select "SI Barcoding Network (SIBN)" from the Individual Projects dropdown. 

Once the project is chosen, the list of expeditions will be populated. Scroll through the list of expeditions until to find the desired expedition (or start typing it in, to bring up a shorter list). 

If a new expedition was just created but it cannot be found in this list, then the data was not successfully uploaded.

If the expedition is found, select it and click the Search button. 

.. image:: /images/fims_database_query.png
  :align: center
  :scale: 40 %
  :target: /en/latest/_images/fims_database_query.png 

This will display an HTML table view of the specimen records in this expedition. Look through this to ensure new data was uploaded successfully.

In the upper right, click the download button to download a fresh Excel spreadsheet of this expedition. However, be advised that the wells will be out of order from the original spreadsheet uploaded and any styling (colors, bold/italics, etc.) will not have been retained. Also, the default spreadsheet name is "geome-fims-output.xlsx", so be sure to rename it with the expedition name immediately. This spreadsheet can be edited with any updated information and re-uploaded as the project progresses and updates are available.
