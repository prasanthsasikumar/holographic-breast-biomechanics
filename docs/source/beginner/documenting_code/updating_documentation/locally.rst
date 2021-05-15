Updating documentation locally using an IDE
-------------------------------------------
Alternatively, you can create a local copy of the project on your computer (forking and cloning the code). You can then edit the source code as desired using your IDE of choice (e.g. PyCharm). You can then follow the best practice guidelines to commit and contribute your code into the project's main repository through a pull request.


.. _Setting up Sphinx in PyCharm:

Updating documentation with PyCharm
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
This section describes how to add a sphinx build configuration to PyCharm:

1. Open Pycharm.

2. :guilabel:`File` →  :guilabel:`Open` → Navigate to your project folder -> Click :guilabel:`Ok`.

3. :guilabel:`Run` → :guilabel:`Edit configurations`.

4. Click the :guilabel:`+` → button on the top left of the window to add a new configuration.

  .. figure:: pycharm_edit_configurations.png
    :width: 300
    :class: with-shadow
    :align: center
    :figclass: align-center

    Add new run configuration in PhyCharm.

5. Select :guilabel:`python docs` → :guilabel:`sphinx task`

  .. figure:: pycharm_add_sphinx_task.png
    :width: 300
    :class: with-shadow
    :align: center
    :figclass: align-center

    Add new run configuration in PhyCharm.

6. Complete the following fields in the configuration task:

  1. :guilabel:`Name`: ``Sphinx task``

  2. :guilabel:`Input`: Select the source directory in the documentation folder (typically, the ``docs/source`` folder).

  3. :guilabel:`Output`: Select the build directory in the documentation folder (typically, the ``docs/build`` folder, if this does not exist copy paste the path you have specified for the Input above, and replace ``source`` with ``build``).

  4. :guilabel:`Python interpreter`: Select your python interpreter.

  5. :guilabel:`Options`: ``-E -a`` (This options forces rebuild of html).

  .. figure:: pycharm_final_sphinx_configuration.png
    :width: 700
    :class: with-shadow
    :align: center
    :figclass: align-center

    Example of a Sphinx task in PhyCharm.

5. Click :guilabel:`Ok`.
6. You can now run the configuration by pressing the green play button.
7. Once you have finished editing the documentation you can commit your changes to your fork of the repository e.g. using Gitkraken, and create a pull request to notify the developers of the main repository that you have changes ready to be pulled into the main repository.

.. seealso::

  Note that Python provides a markdown plugin that allows for dynamic previewing of markdown files as shown in the figure below:

  .. figure:: pycharm_dynamic_markdown_preview.png
    :width: 700
    :class: with-shadow
    :align: center
    :figclass: align-center

    PyCharm Markdown preview plugin.

  .. warning::
    On occasion, a bug in the extension results very high CPU usage, slowing down the performance of PyCharm. To address this issue, you need to close any open Markdown files and restart PyCharm. Alternatively, you can disable the Markdown plugin.
