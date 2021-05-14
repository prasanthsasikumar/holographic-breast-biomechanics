Hosting documentation
=====================

Now that you have created documentation, there are a number of ways that you can share it with others. The most common way is to host the html version of your documentation on a web server. There are a number of services that allow you to host your code depending on whether it is open-source or closed source.

Open-source documentation
-------------------------
Open-source Sphinx documentation can be hosted online using the ReadTheDocs (`readthedocs.org <https://readthedocs.org/>`_) service. If your documentation is stored on a online version control system such as Github, ReadTheDocs provides the ability to automatically update your documentation when you make changes to the source code. This is achieved using a feature called Webhooks. This allows changes to source code via git commits to trigger a rebuild of the documentation.

The following guides show how to host your Sphinx documentation on ReadTheDocs.org:

.. toctree::
   :maxdepth: 3

   readthedocs

Closed-source documentation
---------------------------
Options for hosting close-source (private) Sphinx documentation often require a paid subscription to hosting services. For example the paid version of ReadTheDocs (`readthedocs.com <https://readthedocs.com/>`_ - note the change from `.org` to `.com`), allows for hosting of closed-source Sphinx documentation.