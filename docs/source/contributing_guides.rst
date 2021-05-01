===================
Contributing guides
===================

References
----------
New references can be added in bibtext format to `source/references.bib`.

Please note that the reference keys should be in Snake case (stylized as snake_case) :cite:`snake_case`. This refers to the style of writing in which each space is replaced by an underscore (_) character, and the first letter of each word written in lowercase.

The publication year (if any) should be appended to the reference key.

For example:

.. code-block:: bash

  @Book{1987_nelson,
    author = {Edward Nelson},
    title = {Radically Elementary Probability Theory},
    publisher = {Princeton University Press},
    year = {1987}
  }

.. bibliography:: refs.bib
