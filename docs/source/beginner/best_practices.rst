====================
Best practices (TBC)
====================

Version control
Documentation
Testing

https://github.com/ABI-Software/software-development-guidelines#development-guidelines


Directory setup
===============
The first step in setting up your development environment involves setting up the directory structure that you will use for storing your project files.

Linux & Mac
-----------
Open a terminal and issue the following commands to setup a directory structure for code development.

.. code-block:: bash

  mkdir -p $HOME/opt/ # Location to add the different projects that you will be working.
  mkdir -p $HOME/usr/ # Location where general programs can be installed, e.g. pycharm.
  mkdir -p $HOME/scripts/ # Location of your one off scripts
  mkdir -p $HOME/logs/ # Location of logs from your programs
  mkdir -p $HOME/tmp/ # Location for temporary storage of files/testing bits of code etc

Windows
-------
Create the folders listed in the Linux & Mac section in your `My Documents` folder (ignore the `$HOME` environmental variable). Note that on Windows, you do not need to create a `documents/usr` folder as the Windows `Program Files` directory will serve that purpose.


Replicability
=============

Reproducibility
===============
