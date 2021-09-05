## Adding repositories in your Github account to ReadTheDocs.org
See the following `guide <https://docs.readthedocs.io/en/stable/intro/import-guide.html>`_ for a set of instructions on how to host your open-source Sphinx documentation on ReadTheDocs.org. It will automatically setup a webhook when you import documentation from Github, Bitbucket, or GitLab.

## Adding repositories in a Github organisation to ReadTheDocs.org
Your ReadTheDocs account may not be able to see repositories within a Github organisation you belong to. To address this issue:
1. If you have not already done so, connect your github account to ReadTheDocs by logging into ReadTheDocs and click sign-in via github.
2. Go to your github account settings page.
3. Select `Applications` from the left hand side menu.
4. Click on the `Read The docs Community` row.
5. Under the `Organisation access` section, click the `grant` button next to the organisation that you want ReadTheDocs access.
6. Go to `My Projects` on ReadTheDocs.org.
7. Click `Import a Project`.
8. CLick the refresh button.
9. Navigate through the repositories and you should see repositories under your github organisation (note that your organisation may not show on the organisation filter list, however, they will show up in the list of repositories section of the page.)

## Troubleshooting

### contents.rst not found
By default, readthedocs looks for a contents.rst file. However, by default sphinx creates an index.rst file. Readthedocs will therefore raise the following error:
```bash
Sphinx error:
master file /home/docs/checkouts/readthedocs.org/user_builds/bioengineering-toolbox/checkouts/latest/docs/source/contents.rst not found
```
To address this include the following line in the conf.py file:
```python
# Set the root rst to load. This is required to be named contents to allow
# readthedocs to host the docs using its default configuration.
master_doc = 'index'
```

### [Table width fix for ReadTheDocs Sphinx theme](http://rackerlabs.github.io/docs-rackspace/tools/rtd-tables.html)

### [My ReadTheDocs project isn’t building](http://docs.readthedocs.io/en/latest/faq.html#my-project-isn-t-building-with-autodoc)

First, you should check out the Builds tab of your project. That records all of the build attempts that RTD has made to build your project. If you see `ImportError` messages for custom Python modules, you should enable the virtualenv feature in the Admin page of your project, which will install your project into a virtualenv, and allow you to specify a `requirements.txt` file for your project.

You can create this file using the following steps

> **_NOTE:_**  The following steps assume you have successfully built the Sphinx documentation on your local machine (i.e. that all the required modules are installed on your machine).

Open the conf.py of your sphinx documentation (usually located inside the `docs` folder), and navigate to the extensions section (an example of which  is shown below)
```python
# Add any Sphinx extension module names here, as strings. They can be
# extensions coming with Sphinx (named 'sphinx.ext.*') or your custom
# ones.
extensions = [
   'sphinx.ext.autodoc',
   'sphinx.ext.doctest',
   'sphinx.ext.intersphinx',
   'sphinx.ext.todo',
   'sphinx.ext.coverage',
   'sphinx.ext.imgmath',
   'sphinx.ext.viewcode'
]
```

The Extensions (or in other words - the python modules) that inbuilt into Sphinx are denoted by ``the sphinx.`` prefix. The other python modules will need to be installed when ReadTheDocs builds the documentation on their server.

To see what python modules are currently installed on your machine use the following command in a terminal:

```bash
pip freeze > requirements.txt
```
Search in this file for the items that match the other python modules required by ReadTheDocs (in the example above, search for ``sphinxcontrib``). Move these lines to the top of the file and delete the remaining lines.

Move the `requirements.txt` file in the documentation directory of your repository (commonly labelled `docs`).

Add the location of this file to the ReadTheDocs project admin page and rebuild the documentation on ReadTheDocs.
