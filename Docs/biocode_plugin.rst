.. _biocode_plugin-link:

Connecting with the Biocode Plugin
===========================================

Install the latest version of the Biocode Plugin. Check the :ref:`updates-link` section of the Home Page to see the latest version available and click the link to download the gplugin file if needed. 

To import this gplugin file into Geneious Prime, follow the instructions in the :ref:`plugins-link` section of the previous page.

Once the Biocode plugin has been successfully installed, connect by right-clicking on the Biocode icon in the Sources Panel and click "Login".

.. figure:: /images/biocode_login.png
  :align: center
  :target: /en/latest/_images/biocode_login.png

This will open the *Biocode Connections* window. Click "Add" in the lower left and a new connection will appear that looks like this:

.. figure:: /images/biocode_connection_details_empty.png
  :align: center
  :target: /en/latest/_images/biocode_connection_details_empty.png

Connection Name and Method
--------------------------

Enter a value such as "GEOME FIMS" in the Connection Name so that the plugin saves this information. 


Field Database Connection
--------------------------

In the Field Database Connection section, select "GEOME FIMS" from the dropdown.

.. figure:: /images/biocode_fims_options.png
  :align: center
  :target: /en/latest/_images/biocode_fims_options.png

This will auto-fill the Host box with “https://api.geome-db.org”. Enter the previously assigned GEOME FIMS Username and Password. Make sure to tick the “Save” box to save login information to the plugin.


LIMS Database Connection
-------------------------

In the LIMS location section, start out by selecting "Remote MySQL Database" from the dropdown.

Server Address
	For "Server Address", copy and paste in "nmnh-lims.si.edu".
Port
	For "Port", make sure it is set to "3,306".
Database Name
	For "Database Name", enter "lims".
Username and Password
	Finally, for the "Username" and "Password" boxes, enter the LIMS database Username and Password that were assigned via email by the NMNH LIMS database administrator.

Make sure that the checkbox next to "Save" is ticked.

The fully-completed *Biocode Connections* window should look like this:

.. figure:: /images/biocode_connection_details_completed.png
  :align: center
  :scale: 80 %
  :target: /en/latest/_images/biocode_connection_details_completed.png
  
Click "OK" to log into the Biocode Plugin to be able to utilize the LIMS.
