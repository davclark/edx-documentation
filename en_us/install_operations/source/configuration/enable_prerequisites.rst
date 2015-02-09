.. include:: ../links.rst

.. _Enable Course Prerequisites:

######################################################
Enable Course Prerequisites
######################################################

In the Open edX Birch release, a new feature allows course staff to set
prerequisites for a course. Learners must complete the prerequisite courses
before participating in the course.

To enable this feature on your instance of Open edX, you must enable benable
prerequisites in Studio and the Learning Management System.

For information about prerequisites, see the *Building and Running an
Open edX Course* and *Open edX Learner's* guides.

To enable prerequisites:

#. In the edX Platform installation directory, edit the file
   ``/cms/envs/common.py``

#. Set the values of ``MILESTONES_APP`` and ``ENABLE_PREREQUISITE_COURSES`` to
   ``True``:
   
   .. code-block:: bash

       # Milestones application flag
       'MILESTONES_APP': False,

       # Prerequisite courses feature flag
       'ENABLE_PREREQUISITE_COURSES': False,

#. Save the ``/cms/envs/common.py`` file.
   
#. In the edX Platform installation directory, edit the file
   ``/lms/envs/common.py``

#. Set the values of ``MILESTONES_APP`` and ``ENABLE_PREREQUISITE_COURSES`` to
   ``True``:
   
   .. code-block:: bash

       # Milestones application flag
       'MILESTONES_APP': False,

       # Prerequisite courses feature flag
       'ENABLE_PREREQUISITE_COURSES': False,

#. Save the ``/lms/envs/common.py`` file.

