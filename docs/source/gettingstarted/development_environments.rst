=================================
Software development environments
=================================
This section describes how you can setup your software development environment. This includes setting up a directory structure to organize the storage of your software projects. The next step involves setting up an `integrated development environment (IDE) <https://en.wikipedia.org/wiki/Integrated_development_environment>`_. This is a software application that provides comprehensive facilities to computer programmers for software development. An IDE normally consists of at least a source code editor, build automation tools and a debugger.

Game Engines and IDEs
=====================
Below are a list of development environments that you can use for software development. Supports Windows, Linux and Mac operating systems. Please note that Linux support is new and is a bit buggy as of September 2021.

.. toctree::
   :maxdepth: 1

   development_environments/ides

Why containers are not used?
============================

.. important::
  As part of best practices in software development, it is important that your software environment is replicable. To achieve this, industry standard is to run your IDE within a container or a online-based IDE.
  Unfortunately none of the Game Engines officially support running inside a container(as of September 2021). The next best solution is to replicate the development environment using the exact same version of the software components.

  Using a higher or lower version than the recommended software might lead to incompatibility issues.

  The instructions for downloading a specific version can be found in the `software development container documentation <https://dev-container.readthedocs.io/en/latest/introduction.html>`_.
