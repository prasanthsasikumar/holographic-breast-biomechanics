Click on headings to be directed to answers/more information (if available).

## [1. How to comment?](https://stackoverflow.com/questions/4783814/how-to-comment-a-string-in-restructured-text)
```rest
..
   _This: is a comment!

..
   [and] this!

..
   this:: too!

..
   |even| this:: !
```
Avoid putting comments on the same line as the double dots:
```rest
.. Avoid this type of comment
```
This is considered bad practice since it may lead to unintended consequences if the comment matches a proper markup construct.

## 2. How to include code?

### 2.1. Code blocks
```rest
.. code-block:: language

   code
```

### 2.2. Inline code block with syntax highlighting
First define a custom role. e.g.:

```rest
.. role:: bash(code)
   :language: bash
```

This then allows use inline code e.g.

```rest
Here is some awesome bash code :bash:`a = b + c`.
```

### 2.3. Forcing syntax highlighting for a code snippet.
e.g. for a partial snippet of json code:

```rest
.. code-block:: json-object
    :force:

     "scripts": {
       "build": "webpack",
       "serve": "webpack-dev-server"
     },
```

## [3. How to hyperlink and cross-reference?](https://docs.typo3.org/m/typo3/docs-how-to-document/master/en-us/WritingReST/Hyperlinks.html)

### 3.1. Hyperlinking
```rest
`anchor text <url>`__
```
### 3.2. Referencing section headings
Add `sphinx.ext.autosectionlabel` to extensions in :file:`conf.py`.
Add the following to :file:`conf.py`.
```python
# True to prefix each section label with the name of the document it is in, followed by a colon. For example, index:Introduction for a section called Introduction that appears in document index.rst. Useful for avoiding ambiguity when the same section heading appears in different documents.
autosectionlabel_prefix_document = True
```
Example usage:
```rest
A Plain Title
-------------

This is the text of the section.

It refers to the section title, see :ref:`A Plain Title`.

To reference section headings in other files:
:ref:`path/to/file:Section heading`


```

### 3.3. Cross-Referencing within a document
```rest
:ref:`anchor text <link-target>`
```
### 3.4. Cross-Referencing between documents
```rest
:ref:`anchor text <document-tag:link-target>`
```
Whenever you use the cross-referencing mechanism, you should create a link target for a section chapter, by adding a label before the section header:
```rest
.. _link-target:

Headline
========
```

### 3.5. Referencing external files
Reference files and paths
Use the following syntax to reference files and paths:
```rest
:file:`myfile.txt`
```
This will output: :file:`myfile.txt`.

You can reference paths in the same way:
```rest
:file:`path/to/myfile.txt`
```
This will output: :file:`path/to/myfile.txt`.

### 3.6. Reference an element in a GUI
Use the following syntax to direct a user to click a link or look to a certain area of the GUI:
```rest
:guilabel:`Main Menu`
```
This will output: :guilabel:`Main Menu`.

### 3.7. External files
Text snippets, large blocks of downloadable code, and even zip files or other binary sources can all be included as part of the documentation. To include files as part of the build process, use the following syntax:
```rest
:download:`An external file <readme.txt>`
```

## 3.8. How to create tables?

- [Programtically within .rst files](https://sublime-and-sphinx-guide.readthedocs.io/en/latest/tables.html)
- [Load from csv files](https://tables-with-sphinx.readthedocs.io/en/latest/csv-table.html)

## [3.9. How to add notes and warnings?](http://udig.refractions.net/files/docs/latest/user/docguide/sphinxSyntax.html#notes-and-warnings)

## 3.10. How to number sections?

```rest
.. toctree::
   :numbered: 3
   :maxdepth: 2

   registers/personal
```

More info `here <https://github.com/sphinx-doc/sphinx/issues/5047>`_

## [3.11. How to add images?](https://docs.typo3.org/m/typo3/docs-how-to-document/master/en-us/WritingReST/Images.html)

- Add the `:align: center` and `:figclass: align-center` directive options to center the figure and the caption. More information can be found []here](http://openalea.gforge.inria.fr/doc/openalea/doc/_build/html/source/sphinx/rest_syntax.html#figure-directive).
- Note that the path to the image is relative to the file you are referencing it from.

## 3.12. How to add a bibiliography?
The sphinx [sphinxcontrib-bibtex](https://sphinxcontrib-bibtex.readthedocs.io/en/latest/quickstart.html) extension can be used to insert citations and a bibliography to your documentation. These work similarly to LaTeX’s thebibliography environment and the `\citet` and `\citep` commands.

