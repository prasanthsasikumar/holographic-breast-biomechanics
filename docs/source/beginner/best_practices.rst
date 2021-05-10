==============
Best practices
==============

This section describes best practices across the different aspects of software development.

Directory setup
===============
The first step in setting up your development environment involves setting up the directory structure that you will use for storing your project files.

Linux & Mac
-----------
Open a terminal and issue the following commands to setup a directory structure for code development.

.. code-block:: bash

  mkdir -p $HOME/work/ # Location to add the different projects that you will be working.
  mkdir -p $HOME/usr/ # Location where general programs can be installed, e.g. pycharm.
  mkdir -p $HOME/scripts/ # Location of your one off scripts
  mkdir -p $HOME/logs/ # Location of logs from your programs
  mkdir -p $HOME/tmp/ # Location for temporary storage of files/testing bits of code etc

Windows
-------
Create the folders listed in the Linux & Mac section in your ``My Documents`` folder (ignore the :envvar:`$HOME` environmental variable). Note that on Windows, you do not need to create a ``documents/usr`` folder as the Windows ``Program Files`` directory will serve that purpose.

Development process
===================

1. Create a Github ``issue`` on the main github repository for the code project you are interested to discuss the changes you are proposing. You can use the Github ``issue`` to highlight any problems you are facing when using the code, or indicate what you want to contribute. Once you have received feedback to you can then start editing the code.

2. Fork the repository (if you already have a fork, then ensure that you have pulled in any of the latest commits).

2. Create a branch to work on the feature that you are developing/bugfix.

3. Commit changes.

  .. important::
    Mention the issue number to highlight the progress you have made to addressing the issue. These will get automatically collated on the issue page on github, and will be available for code reviewers in future steps.

4. Once you have finished the feature/bugfix create a ``pull request`` from your fork into the main repository. One of their developers will then review your changes. You can make additional commits (mentioning the issue number) to address any requests by the review. Once the review process is completed, the code will be pulled into the main repository.

Gitkraken's GUI is an easy to use tool for managing git repositories and will allow you to perform all the above steps. See the `Gitkraken support pages <https://support.gitkraken.com/start-here/interface/>`_ for more information.


Replicability (TBC)
===================

Reproducibility (TBC)
=====================


Additional resources
====================

- https://github.com/ABI-Software/software-development-guidelines#development-guidelines