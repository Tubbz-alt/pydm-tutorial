PyDM Launcher
=============

PyDM provides a launcher that makes it easier for users to quickly run UI files as well as code based screens.
The launcher is responsible for setting up the Python logging module but it mainly parses the command line parameters
and send them to the instantiated PyDMApplication.

The Launcher is available for Linux, OSX and Windows and it can be called using the command line:

.. code-block:: bash

   pydm

This will result in the PyDM Main Window being displayed.

.. figure:: /_static/intro/main_window.png
   :scale: 75 %
   :align: center
   :alt: PyDM Main Window

Command Line Arguments
----------------------

PyDM Launcher accept many command line arguments, here they are:

.. code-block:: bash

   pydm [-h] [--perfmon] [--hide-nav-bar] [--hide-menu-bar]
        [--hide-status-bar] [--read-only]
        [--log_level {DEBUG,INFO,WARNING,ERROR,CRITICAL}] [-m MACRO]
        [displayfile] ...



Where:

=========================  =============================================================================
Argument                   Description
=========================  =============================================================================
-h, --help                 Show the help message and exit
--perfmon                  Enable performance monitoring, and print CPU usage to the terminal
--hide-nav-bar             Start PyDM with the navigation bar hidden
--hide-menu-bar            Start PyDM with the menu bar hidden
--hide-status-bar          Start PyDM with the status bar hidden
--read-only                Start PyDM in a Read-Only mode
--log_level                Configure the level of the display logger.
-m MACRO, --macro MACRO    Specify macro replacements to use, in JSON object format
displayfile (positional)   A PyDM file to display. Can be either a Qt (.ui) file or a Python (.py) file
display_args (positional)  Arguments to be passed to the PyDM client application and displays.
=========================  =============================================================================

.. note::
   It is not mandatory for you to use the PyDM Launcher to run your screen but keep in mind that not using it means that
   you will need to handle command line arguments, logging setup and the instantiation of the PyDMApplication at your own
   code.