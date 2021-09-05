Creating new documentation with Sphinx
======================================

This section describes how sphinx documentation can be created for your project. Typically this documentation would be generated within a code repository.

Setting up a Sphinx project
---------------------------
1. Follow the quick-start instructions on the `official sphinx documentation page <https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html#quick-start>`_
2. During this process, it will ask ``Separate source and build directories (y/n)``. Select yes.

3. You can now add new reST source files and place them in the ``docs/source`` folder.

4. Add the filenames of these new source file to the ``index.rst`` file in the ``docs/source`` folder.

To make this process easier, we have provided a `template software project <https://github.com/Research-software-development-resources/template-project>`_ on Github that you can use to get started. Download and copy the ``docs`` folder from this repository


Building Sphinx documentation
-----------------------------

From the command line
---------------------
1. In a terminal, change directory to the folder where the sphinx documentation was generated (ie the ``docs`` folder):

  .. code-block:: bash

    cd path/to/docs

2. Enter the following command.

  .. code-block:: bash

    make html

3. You can then open the html version of the documentation by opening  ``/path/to/docs/build/index.html`` in your browser of choice e.g. Google Chrome.

From IDEs
---------
For more information on how to build documentation from IDEs such as PyCharm, see the ``Updating documentation`` Section of this tutorial.

FAQs
====
This section provides documentation on how to use reStructuredText and Markdown with Sphinx.

reStructuredText with Sphinx FAQ
--------------------------------

.. toctree::
   :maxdepth: 3

   rest

Markdown with Sphinx FAQ
------------------------

.. toctree::
   :maxdepth: 3

   markdown