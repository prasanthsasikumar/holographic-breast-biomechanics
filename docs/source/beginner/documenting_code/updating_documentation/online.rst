Updating documentation online
-----------------------------
You can directly edit existing documentation online, for example on github. This approach allows you to contribute changes using only a web browser.

1. Navigate to the repository of interest.
2. If the repository does not belong to you, fork the repository, (part of the best practice guidelines). You can do this by clicking on the fork icon on the top right of the repository. This will create a copy of the repository on your github account.
3. In the project, select the file that you wish to edit (e.g. a file ending with .md (Markdown) or .rst (reST)). The rendered preview of the file will appear.
4. Click on the pencil button as shown in the screenshot below to edit the file.

  .. figure:: editing_docs_on_github.png
    :width: 600
    :class: with-shadow
    :figclass: align-center

    Editing documentation on github.

  This will open the editor mode showing the file in markup format.

  .. figure:: edit_mode_on_github.png
    :width: 600
    :class: with-shadow
    :align: center
    :figclass: align-center

    Editing mode on github.

5. Make edits.
6. Preview edits by clicking on the Preview tab.

  .. figure:: previewing_doc_edits_on_github.png
    :width: 600
    :class: with-shadow
    :align: center
    :figclass: align-center

    Previewing changes on github.

6. Once you are finished, scroll to the bottom of the page to the Section named ``Commit changes``.

  1. Add a title to your commit that summarises the change that you made.

  2. Add an optional extended description.

  .. figure:: committing_changes_on_github.png
    :width: 600
    :class: with-shadow
    :align: center
    :figclass: align-center

    Committing changes on github.

7. Decide whether you want to commit directly to the ``master`` branch or make the commit to a new branch and start a pull request (best practice guidelines recommend the latter option.
8. Create a pull request from your fork to the main repository. This will allow the owner of the main repository to review your changes and determine whether it can be contributed back into the main repository.

.. important::
   See the best practices guide for more information on the how to contribute software projects.

For additional information see the following `outline on contributing to documentation via github <https://docs.typo3.org/m/typo3/docs-how-to-document/master/en-us/WritingDocsOfficial/GithubMethod.html#docs-contribute-github-method>`_.