Documentation generation tools
==============================
Rather than having to manually open reStructuredText or Markdown text files individually, we can use a documentation generation tool to help us organise and render our documentation in HTML or PDF format.

`Sphinx <https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html>`_ is a powerful documentation generation tool that uses the `Docutils python library <http://docutils.sourceforge.net/>`_ for processing documentation mark up language files. It has many features for writing technical documentation including:

- generates web pages, printable PDFs, documents for e-readers (ePub), and more, all from the same source files;
- supports reStructuredText (default) or Markdown (enabled via an extension);
- a system for cross-referencing documentation;
- ability to embed existing code from source files into documentation (without needing to duplicate the code); and
- support for extensions (e.g. adding bibliography support, automated creation of API's from docstrings).

This documentation can then be hosted on the web for others to access. For example, third-party services such as `ReadTheDocs.org <https://readthedocs.org/>`_ provides free hosting of open-source documentation (see the Hosting documentation Section for more information). Other options are available for hosting private source code.

Here are some examples of open-source code documented with Sphinx and hosted on ReadTheDocs.

- https://opencmiss-iron-tutorials.readthedocs.io
- http://libcellml.readthedocs.io/
- http://morphic.readthedocs.io/


Extra reading
-------------
To find out about the differences between reST, docutils, readthedocs, sphinx, and extensions, see this `link <http://www.git-pull.com/code_explorer/rst-docutils-sphinx-readthedocs.html#rest-docutils-sphinx-readthedocs>`_.

References
----------

.. bibliography:: ../../refs.bib
  :style: alpha