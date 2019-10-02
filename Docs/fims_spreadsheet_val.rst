GeOMe FIMS spreadsheet validation and upload
======================================

Validating and uploading the spreadsheet
---------------------------------------------

If SIBN is performing the lab work for your project, please only work through the “validation” portion of this section and then email the spreadsheet to your project manager. We will take care of uploading everything for you. 

Once we have a spreadsheet fully populated, our next step will be to validate and possibly upload the spreadsheet to the GeOMe FIMS database. (Again, if SIBN will be conducting your lab work, please only validate the spreadsheet, then forward it to your project manager.) The validation step checks every specimen record to make sure that they meet the set of rules established by the project. 

Validation without loading
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1.	Go to https://geome-db.org/ and click on Workbench. 
2.	If you are already logged into GeOMe, you will click Load Data at the top left, and then tick the “Only validate data” box at the top of the Load Data screen.
3.	Or, if you are not logged in, click Validate Data at the top left. 
4.	Where it says ‘Excel Workbook’, click the Browse button to select your spreadsheet. 
5.	Select the pre-existing expedition called “_SIBN_Validation” and click the Validate button.
6.	If your spreadsheet passes validation, great! Forward it on to your SIBN program manager and skip the rest of this section. Otherwise, please resolve the errors you are given and try validating again. 

*Note: To pass validation, your data must be in a tab named Samples within the spreadsheet.*

.. image:: /images/fims_validation.png
  :align: center
  :target: /en/latest/_images/fims_validation.png

Validation and loading
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1.	Go to https://geome-db.org/, click on the user profile image with the down-pointing caret at the top, and then click on Sign in. 
2.	Log in with your pre-assigned GeOMe username and password. (You do not need to log in to validate your spreadsheet, but you must be logged in to upload it to the database). 
3.	After logging in, go to Workbench and then click Load Data at the top left. 
4.	On the Load Data page, for ‘FIMS Data’ click the Browse button to select your spreadsheet. 
	
	a) If this is the first time you have uploaded this plate to GeOMe, you will need to assign an “Expedition Name”. In the Expedition Name drop-down that appears, click the plus sign to the right of the box and enter your plate name. (The same plate name should go in Expedition Title and Expedition Code.) Remember to follow the :ref:`conventions-link`, and make sure not to repeat a previously created expedition code. **Note: While the expedition title can be modified at any time, the expedition code is a unique identifier and cannot be changed.
	
	b) If you are adding or updating data you have previously uploaded, simply select the associated plate name from the Expedition Name drop-down. **Note: do not click “Replace expedition data” unless you want all of the previous data uploaded to be replaced with the new data. 
5.	If you are ready to upload your spreadsheet, click the Load button. If there are no errors, the screen should return a “Successfully Validated!” message.

*Note: To pass validation, your data must be in a tab named Samples within the spreadsheet. If you have already tried to upload data and validation failed, you may have to tick the box that says “Replace expedition data” when uploading it again.* 


.. image:: /images/fims_validation_upload.png
  :align: center
  :target: /en/latest/_images/fims_validation_upload.png

Can I add a few records to an existing dataset by just uploading those new records?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

YES! As long as you do not tick the “Reload Data” option, GeOMe will add new data to existing data. Just make sure you select the correct expedition to add the records to.

Check that the spreadsheet was successfully uploaded
----------------------------------------------------

Even though we got a success message, let’s make sure your data made it into the database successfully. This will also show how to retrieve data from the FIMS if you ever want to make changes. Click on the Query button at the top of the screen.

On the Query page, you will be able to view the data from any dataset on any of the projects in the GeOMe FIMS. This is why it is so important not to include sensitive information (such as highly accurate GPS coordinates) in spreadsheet uploads. To see the dataset we just uploaded, first click on “Switch to Advanced Search” in the top right of the search screen. Then select SI Barcoding CBOL from the Individual Projects dropdown. Once the project is chosen, the list of datasets will be populated. Scroll through the list of datasets until you find the one you just created (or start typing it in, to bring up a shorter list). If you do not see it in this list, then your data was not successfully uploaded.

Select the dataset you just uploaded and click the Search button. 

.. image:: /images/fims_database_query.png
  :align: center
  :scale: 25 %
  :target: /en/latest/_images/fims_database_query.png 

This will display an HTML table view of the specimen records in this dataset. It will be incredibly hard to read and scroll through, but be happy it made it in there. 

You can click the Download button to download a fresh Excel spreadsheet of this dataset. However, be advised that the wells are out of order and that you will lose any styling (colors, bold/italics, etc.) from when you originally uploaded the spreadsheet. Also, the default spreadsheet name is "geome-fims-output.xlsx", so be sure to rename it with your dataset name immediately.
