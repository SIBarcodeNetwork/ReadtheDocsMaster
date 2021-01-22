.. _biocode_plugin-link:

Connecting with the Geneious Biocode Plugin
===========================================

BWP Biocode Plugin connection details
-------------------------------------

Install the latest version of the Biocode Plug-in. Check the :ref:`updates-link` section of the Home Page to see the latest version available. If you do not have the latest version, then follow the instructions in the :ref:`plugins-link` section of the previous page.

Once the Biocode plugin has been successfully installed, you can now connect by right-clicking on the Biocode icon in the Sources panel and click "Login".

.. figure:: /images/biocode_login.png
  :align: center
  :target: /en/latest/_images/biocode_login.png

This will open the Biocode Connections window that looks like this:

.. figure:: /images/biocode_connection_details_empty.png
  :align: center
  :target: /en/latest/_images/biocode_connection_details_empty.png

Connection Name and Method
~~~~~~~~~~~~~~~~~~~~~~~~~~

Enter a value in the Connection Name so that the plug-in saves this information. 

Field Database Connection
~~~~~~~~~~~~~~~~~~~~~~~~~

In the Field Database Connection section, select "GeOMe FIMS" from the dropdown.

.. figure:: /images/biocode_fims_options.png
  :align: center
  :target: /en/latest/_images/biocode_fims_options.png

This will auto-fill the Host box with “https://api.geome-db.org”. Enter the FIMS Username and Password assigned to you. Make sure to tick the “Save” box to save your login information to the plugin.


LIMS Database Connection
~~~~~~~~~~~~~~~~~~~~~~~~

In the LIMS Location section, start out by selecting "Remote MySQL Database" from the dropdown.

Server Address
	For "Server Address", copy and paste in "nmnh-lims.si.edu".
Port
	For "Port", make sure it is set to "3,306".
Database Name
	For "Database Name", enter "lims".
Username and Password
	Finally, for the "Username" and "Password" boxes, enter the LIMS database Username and Password that John Keltner assigned to you via email.

Make sure that the checkbox next to "Save" is ticked.

Your fully-completed Biocode Connection window should look like this:

.. figure:: /images/biocode_connection_details_completed.png
  :align: center
  :scale: 50 %
  :target: /en/latest/_images/biocode_connection_details_completed.png
