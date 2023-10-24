GWS Structure
=============

Overview
--------

The GWS can be found in the ``/gws/pw/j07`` directory on JASMIN, and is split into two volumes - ``ncas_obs_vol1`` and ``ncas_obs_vol2``. Within these volumes are directories for each of the AMOF atmospheric observatories, one for mobile instruments, and one for FAAM, with ``amf`` (soon to be ``mobile``), ``bttao``, ``cdao``, ``cvao``, ``faam``, ``iao``, and ``wao`` in ``ncas_obs_vol1``, and ``cao`` in ``ncas_obs_vol2``. Each of these observatory directories have a number of folders for raw data, processed data, software, and sending data to the CEDA archive.

**INSERT PRETTY PICTURE**

Raw Data
--------
Raw data is the data that comes out of the instrument, prior to any processing or calibration work. Within this folder is a directory for each instrument associated with the observatory, using the instrument's unique AMOF instrument name. These instrument folders contain two folders:

- ``incoming`` - a writeable directory for raw data to be uploaded into. Once the instrument scientist is happy the data is correct, it is moved into the ``data`` directory and made read only.
- ``data`` - read-only directory containing raw data from the instrument. Within this folder, data should be split into folders related to the project the data relates to, in the format ``<start_date>_<project_name>`` (see `Project Folder`_ for more information).


Software
--------

Processing
----------

Tools
-----

Additional Data
---------------

Upload
------

Logs
----

Public
------

GWS_scripts
-----------

Project Folder
--------------
In a number of places throughout the GWS, instrument data is stored within a project folder, which is named in the format ``<start_date>_<project_name>``. This project folder helps to keep related data together through the GWS, and helps place it in the right place when uploaded to the CEDA archive.

- ``<start_date>`` is the first date on which the instrument collected data during the project, and must be in YYYYmmdd format.
- ``<project_name>`` is the name, or abbreviated name, of the project during which data was collected. In the case of long term observations taken at an observatory unrelated to a specific project, ``longterm`` should be used for static instruments (i.e. instruments that are part of the observatory) or the abbreviated observatory name (e.g. ``iao``) for mobile instruments.
