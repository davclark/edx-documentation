.. include:: ../links.rst

.. _Add the Google Drive and Google Calendar XBlock:

######################################################
Add the Google Drive and Google Calendar XBlock
######################################################

In the Open edX Birch release, course staff can embed Google calendars and
Google Drive files in courseware.

To enable this feature on your instance of Open edX, you install the
:ref:`Google Drive XBlock`.

For information about using Google calendars and Google Drive files in courses,
see the *Building and Running an Open edX Course* guide.

To install the Google Drive XBlock:

#. In the edX Platform installation directory, edit the file
   ``requirements/edx/github.txt``

#. Add a the line to add the Google Drive XBlock:
   
   .. code-block:: bash

     git+https://github.com/edx-solutions/xblock-google-drive.
     git@????????????????????????????????????#egg=xblock-google-drive

#. Save the ``requirements/edx/github.txt`` file.
