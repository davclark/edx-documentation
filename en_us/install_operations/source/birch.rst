.. include:: links.rst

.. _Open edX Birch Release:

########################################
Open edX Birch Release
########################################

See:

* `What's Included in Birch`_
* `What's is the Birch GIT Tag`_
* `Installing the Birch Release`_
* `Upgrading from Aspen to Birch`_

******************************
What's Included in Birch
******************************

The Open edX Birch release contains several new features for students, course
staff, and developers.  See the Open edX Release Notes for more details. (LINK)

.. Note:: 
 There are several new features in the Birch release that are available, but
 not configured in new installations.  See:

 * :ref:`Add the Google Drive and Google Calendar XBlock`.
 * :ref:`Enable Course Prerequisites`
 * :ref:`Enable Entrance Exams`

******************************
What's is the Birch Git Tag
******************************

The Git tag for the Birch release is **named-release/birch.rc1**.

.. confirm

******************************
Installing the Birch Release
******************************

You can install the Open edX Birch release with :ref:`Devstack <Installing the
Open edX Developer Stack>` or :ref:`Fullstack<Installing Open edX Fullstack>`.

Review those instructions for each option, then choose the option that best
meets your needs. Ensure you install the required software to run run the edX
Platform.

If you are upgrading from the Aspen release, see `Upgrading from Aspen to
Birch`_.

For new installations, follow the steps below:

#. `Download the Vagrant Box`_
#. `Add the Vagrant Box`_
#. `Install the Vagrant Box`_

=========================
Download the Vagrant Box
=========================

You must download the Vagrant box from BitTorrent to the computer where you
intend to install the edX Platform.

Download the Vagrant box for the option you selected:

* `Devstack <Birch Devstack>`_
* `Fullstack <Birch Fullstack>`_

See `Vagrant's documentation on boxes`_ for more information.

=========================
Add the Vagrant Box
=========================

You must add the box to Vagrant:

* For Devstack installations, enter:

   .. code-block:: bash

     $ vagrant box add /path-to-downloaded-box/vagrant-images-20150203-birch-
     devstack.box.torrent --name birch-devstack-rc1

* For Fullstack stack installations, enter:

   .. code-block:: bash

     $ vagrant box add /path-to-downloaded-box/vagrant-images-20150204-birch-
     fullstack.box.torrent --name birch-fullstack-rc1

.. confirm names

====================================
Update the OPENEDX_RELEASE Variable
====================================

Before installing the Vagrant box, you must change the value of the
`OPENEDX_RELEASE` variable in the `Vagrantfile` to the GIT tag for the Birch
release:

.. code-block:: bash

  OPENEDX_RELEASE=named-release/birch.rc1


=========================
Install the Vagrant Box
=========================

When you have completed the previous steps, install the Birch release by
following the installation instructions for :ref:`Devstack <Installing the Open
edX Developer Stack>` or the :ref:`Fullstack <Installing Open edX Fullstack>`.


******************************
Upgrading from Aspen to Birch
******************************

You can upgrade your Open edX instance that is running the Aspen release to the
Birch release.

.. note::  
  The upgrade scripts provided are verified only for upgrading instances
  running the Aspen release. If you are running any other version of the Open
  edX Platform, edX does not guarantee that the upgrade scripts will work.

.. caution:: 
  Before upgrading your Open edX instance, back up all data and configuration
  files.

On the computer or virtual machine running the Aspen release of Open edX, run
the upgrade script for your type of installation:

* For Devstack, run the ``migrate-devstack.sh`` script.

* For Fullstack, run the ``migrate-fullstack.sh`` script.
  
The script creates a temporary directory in which it upgrades Open edX, then
cleans up extra files and directories when it completes.

After upgrading Open edX to the Birch release, run the edX Platform and verify
that the upgrade script worked correctly.
