================
Documenting code
================

The objectives of this tutorial are to familiarise yourself with:

- principles for creating good documentation;

- plain text markup languages commonly used for writing documentation (Markdown and reStructuredText);

- tools for processing plain text documentation and generating output in html or pdf formats (Sphinx);

- online services for hosting documentation (ReadTheDocs); and

- methods for contributing to documentation.

Introduction
============
Documentation needs to include and be structured around its **four different functions**: *tutorials*, *how-to guides*, *technical reference* and *explanation*. People working with software need these four different kinds of documentation at different times, in different circumstances - so software usually needs them all, and they should be integrated into your documentation :cite:`documentation_by_divio`.

.. list-table::
   :widths: 16 21 21 21 21
   :header-rows: 1

   * - \
     - `Tutorials <https://documentation.divio.com/tutorials/#tutorials>`_
     - `How-to guides <https://documentation.divio.com/how-to-guides/#how-to>`_
     - `Reference <https://documentation.divio.com/reference/#reference>`_
     - `Explanation <https://documentation.divio.com/explanation/#explanation>`_
   * - *oriented to*
     - learning
     - a goal
     - information
     - understanding
   * - *must*
     - allow the newcomer to get started
     - show how to solve a specific problem
     - describe the machinery
     - explain
   * - *its form*
     - a lesson
     - a series of steps
     - dry description
     - discursive explanation
   * - *analogy*
     - teaching a small child how to cook
     - a recipe in a cookery book
     - a reference encyclopaedia article
     - an article on culinary social history

For more information, see the following `guide by Daniele Procida <https://documentation.divio.com/>`_.

Additional resources:

- `Tips <https://docs.typo3.org/m/typo3/docs-how-to-document/master/en-us/WritingContent/WritingContentTips.html>`_

- `Neutrality and inclusivity <https://github.com/ABI-Software/software-development-guidelines#neutrality-and-inclusivity>`_

Languages
=========
Markdown and reStructuredText (RST) are examples of lightweight markup languages that are commonly used for writing documentation. These languages aim to be easily readable by human programmers who are reading and writing source code. The documentation is often written as plain text files.

Markdown
--------
Markdown’s primary objective was to create a syntax for plain text that could be easily converted to HTML :cite:`markdown`. It is considered as an easy to use language and is the default markup language for creating StackOverflow or Reddit posts, GitHub readme files, and documenting Jupyter notebooks. However, it suffers from lack of a comprehensive specification (standardisation) which is important for implementing technical documentation.

- `Syntax guide and best practices <https://www.markdownguide.org/basic-syntax/>`_

reST
----
reStructuredText on the other hand has more built-in features for writing more complex documents, is more standardized, and has built-in support for extensions. Therefore, it is often used for creating fully fledged documentation for small or large software projects. It is used primarily in the Python programming language community for technical documentation.

- `Syntax guide <http://rest-sphinx-memo.readthedocs.io/en/latest/ReST.html>`_
- `Style guide <https://docs.typo3.org/m/typo3/docs-how-to-document/master/en-us/GeneralConventions/Index.html>`_
- `Cheatsheet <https://docs.typo3.org/m/typo3/docs-how-to-document/master/en-us/WritingReST/CheatSheet.html>`_

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

Getting started with Sphinx
---------------------------
.. toctree::
   :maxdepth: 3

   documenting_code/sphinx

reStructuredText with Sphinx FAQ
--------------------------------

.. toctree::
   :maxdepth: 3

   documenting_code/rest

Markdown with Sphinx FAQ
------------------------

.. toctree::
   :maxdepth: 3

   documenting_code/markdown

Hosting documentation
=====================
Now that you have created documentation, there are a number of ways that you can share it with others. The most common way is to host the html version of your documentation on a web server. There are a number of services that allow you to host your code depending on whether it is open-source or closed source.

Open-source documentation
-------------------------
Open-source Sphinx documentation can be hosted online using the ReadTheDocs (`readthedocs.org <https://readthedocs.org/>`_) service. If your documentation is stored on a online version control system such as Github, ReadTheDocs provides the ability to automatically update your documentation when you make changes to the source code. This is achieved using a feature called Webhooks. This allows changes to source code via git commits to trigger a rebuild of the documentation.

The following guides show how to host your Sphinx documentation on ReadTheDocs.org:

.. toctree::
   :maxdepth: 3

   documenting_code/readthedocs

Closed-source documentation
---------------------------
Options for hosting close-source (private) Sphinx documentation often require a paid subscription to hosting services. For example the paid version of ReadTheDocs (`readthedocs.com <https://readthedocs.com/>`_ - note the change from `.org` to `.com`), allows for hosting of closed-source Sphinx documentation.

Collaboratively updating documentation
======================================
Once you have created the documentation, there are a number of ways to allow others to update it.

.. note::
   As part of best practice guidelines, it is recommended to use a version control system for tracking commits to your code and host your code on a online version control service such as github. If you are The following how-to-guides assume you are following these guidelines.

Updating documentation online
-----------------------------
You can directly edit existing documentation online, for example on github. This approach allows you to contribute changes using only a web browser.

1. Navigate to the repository of interest.
2. If the repository does not belong to you, fork the repository, (part of the best practice guidelines). You can do this by clicking on the fork icon on the top right of the repository. This will create a copy of the repository on your github account.
3. In the project, select the file that you wish to edit (e.g. a file ending with .md (Markdown) or .rst (reST)). The rendered preview of the file will appear.
4. Click on the pencil button as shown in the screenshot below to edit the file.

  .. figure:: documenting_code/editing_docs_on_github.png
    :width: 600
    :class: with-shadow
    :figclass: align-center

    Editing documentation on github

  This will open the editor mode showing the file in markup format.

  .. figure:: documenting_code/edit_mode_on_github.png
    :width: 600
    :class: with-shadow
    :align: center
    :figclass: align-center

    Editing mode on github

5. Make edits.
6. Preview edits by clicking on the Preview tab.

  .. figure:: documenting_code/previewing_doc_edits_on_github.png
    :width: 600
    :class: with-shadow
    :align: center
    :figclass: align-center

    Previewing changes on github

6. Once you are finished, scroll to the bottom of the page to the Section named `Commit changes`.

  1. Add a title to your commit that summarises the change that you made.

  2. Add an optional extended description.

  .. figure:: documenting_code/committing_changes_on_github.png
    :width: 600
    :class: with-shadow
    :align: center
    :figclass: align-center

    Committing changes on github

7. Decide whether you want to commit directly to the `master` branch or make the commit to a new branch and start a pull request (best practice guidelines recommend the latter option.
8. Create a pull request from your fork to the main repository. This will allow the owner of the main repository to review your changes and determine whether it can be contributed back into the main repository.

.. note::
   This step assumes that either you own the main code repository, or you have already notified the developers of the repository you are creating the pull request to. Otherwise it will look very 'random'. In the case where you have not discussed the changes you are proposing  with the developers of the main repository, it is best practice to first discuss with them. This can be achieved by creating an `issue` on the main github repository for the code project you are interested in. You can highlight the issue you are having, or indicate what you want to contribute. When you commit changes, you can then mention the issue number to highlight the progress you have made to addressing the issue. These will get automatically collated on the issue page on github, and will be available for code reviewers to see when you create your pull request.

For additional information see the following `outline <https://docs.typo3.org/m/typo3/docs-how-to-document/master/en-us/WritingDocsOfficial/GithubMethod.html#docs-contribute-github-method>`_.

Updating documentation locally
------------------------------
Alternatively, you can create a local copy of the project on your computer (forking and cloning the code), and edit the source code as desired using your IDE of choice (e.g. PyCharm). You can then follow the best practice guidelines to commit and contribute your code into the project's main repository through a pull request.

Extra reading
=============
To find out about the differences between reST, docutils, readthedocs, sphinx, and extensions, see this `link <http://www.git-pull.com/code_explorer/rst-docutils-sphinx-readthedocs.html#rest-docutils-sphinx-readthedocs>`_.

References
==========

.. bibliography:: ../refs.bib
  :style: alpha