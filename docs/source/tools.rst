GWS Tools
=========

.. _upload to ceda paragraph:

Upload to CEDA
--------------
When the instrument scientist has created files in the :ref:`processing folder <processing folder paragraph>` ready to be archived on CEDA, a script is available that uses :ref:`checksit <checksit paragraph>` to check the formatting of the files, before moving them into the :ref:`upload folder <upload folder paragraph>` from where they will be moved to the CEDA system. This script can be used on one file, multiple files, or an entire directory::

  cd /gws/pw/j07/ncas_obs_vol1/scripts/transfer_to_upload
  ./transfer_to_upload /gws/pw/j07/ncas_obs_vol1/iao/processing/ncas-aws-10/20010101_longterm

where ``/gws/pw/j07/ncas_obs_vol1/iao/processing/ncas-aws-10/20010101_longterm`` is a directory that has netCDF files in structured within ``yyyy/mm`` folders as described in the :ref:`processing folder <processing folder paragraph>` section, and could be replaced by a file or a space-separated list of files.


.. _public html paragraph:

Public HTML
-----------
A public HTML space is `available online`_, for the purpose of sharing small files from the group workspace, such as log files, small data files that need to be quickly shared, or latest plots of data. Note that this space is NOT intended for hosting websites or building tools and applications. See `this article from JASMIN`_ for more details.



.. _github paragraph:

GitHub
------
All instruments have three separate GitHub repositories within the `NCASUK GitHub organisation`_. These take the form
::

  instrument-software
  instrument-tools
  instrument-additionaldata

where ``instrument`` is the unique name given to each NCAS instrument. These repositories are ready to use on JASMIN in the :ref:`software <software folder paragraph>`, :ref:`tools <tools folder paragraph>`, and :ref:`additional data <additionaldata folder paragraph>` folders. Each instrument scientist will need to have their own GitHub account and let the NCAS IT team know which instrument repositories they require access to.


.. _checksit paragraph:

checksit
--------
An installation of checksit_ is available on JASMIN. checksit is a compliance checker being designed to check data from NCAS instruments meets the format required by the relevant NCAS data standard. More information on the NCAS data standards can be found on the `NCAS Data Activity`_ documentation. This installation of checksit is used in the :ref:`tools that send data to the CEDA arrivals area<upload to ceda paragraph>`. checksit can be used by anyone with GWS access by following these instructions::

  /apps/jasmin/community/checksit

More information about this install can be found on the `JASMIN help docs`_.

.. _checksit: https://checksit.readthedocs.io
.. _this article from JASMIN: https://help.jasmin.ac.uk/article/202-share-gws-data-via-http
.. _available online: https://gws-access.jasmin.ac.uk/public/ncas_obs/
.. _NCASUK GitHub organisation: https://github.com/ncasuk
.. _NCAS Data Activity: https://sites.google.com/ncas.ac.uk/ncasobservations/home/data-project/
.. _JASMIN help docs: https://help.jasmin.ac.uk/article/5131-checksit
