=================================
Software development environments
=================================
This section describes how you can setup your software development environment. This includes setting up a directory structure to organise the storage of your software projects. The next step involves setting up an `integrated development environment (IDE) <https://en.wikipedia.org/wiki/Integrated_development_environment>`_. This is a software application that provides comprehensive facilities to computer programmers for software development. An IDE normally consists of at least a source code editor, build automation tools and a debugger.

IDEs
====
Below are a list of cross-platform IDEs that you can use for software development. Cross-platform IDEs will work across Linux, Mac, and Windows.

.. toctree::
   :maxdepth: 1

   development_environments/ides

Using IDEs in containers
========================

.. important::
  As part of best practices in software development, it is important that your software environment is replicable. To achieve this, it is recommended to run your IDE within a container or a online-based IDE.

  We have setup a container-based development environment to help researchers develop software for their projects. This development environment includes commonly used IDEs including PyCharm, Visual Studio Code, and JupyterLab and can be run on Linux, Mac, or Windows. This provides a replicable sandboxed environment for you to develop your software.

  The instructions for running these IDEs within a container are provided in the link below.

.. toctree::
   :maxdepth: 3

   development_environments/containers

