## 1. How to enable support for Markdown files with Sphinx?
By default, sphinx recognises [RestructuredText](https://en.wikipedia.org/wiki/ReStructuredText). In order to use Markdown in Sphinx, an extension needs to be added to Sphinx. Sphinx supports an unambiguous version of Markdown called [CommonMark](https://commonmark.org/) which addresses many of [Markdown's limitations](https://www.ericholscher.com/blog/2016/mar/15/dont-use-markdown-for-technical-docs/).

CommonMark can be enabled in Sphinx by including the `Recommonmark` extension in the Sphinx `conf.py`. See [official sphinx documentation page](https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html#using-markdown-with-sphinx) for instructions on how to enable this sphinx extension.

## 2. How to add new Markdown files?
A new markdown file can be added to your project as described below (ensure that the `Recommonmark` Sphinx extension has been enabled as described in the previous section).

1. Create a new text file with the `.md` extension in appropriate folder within the standard sphinx `docs/source` folder, e.g. `docs/source/my/folder/file.md`.

2. This new file can be added to the main Sphinx table of contents by adding the filename to the `index.rst` file in the `docs/source/` folder as shown below:
    ```rest
    ===========================
    Welcome to my documentation
    ===========================

    .. toctree::
       :maxdepth: 2
       :caption: Contents:

       my/folder/file
    ```

## 3. How to Link to heading sections in other markdown files?
When writing documentation, it might be useful to reference headings sections in other markdown files. This can be enabled using the following [instructions](https://recommonmark.readthedocs.io/en/latest/#linking-to-headings-in-other-files).

For example, to link to a section named `# My subtitle` in a file located in `/path/to/file.md`, relative to the `docs/source` folder.
```md
[text for the link](/path/to/file:My%20Subtitle)
```
> **_NOTE:_**
>1. Any spaces in headings need to be replaced by `%20`.
>2. The .md file extension should not be included in the path to the file.

## 4. How to add notes and warnings?

Notes:
```
> **_NOTE:_**  Add text here
```
Warnings:
```
> **_WARNING:_**  Add text here
```
