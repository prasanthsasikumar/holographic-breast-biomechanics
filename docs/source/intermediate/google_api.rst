==========================================================
Interacting with google sheets and google drive via python
==========================================================

The google python API can be used to read, write data to google sheets and google drive. For example, processed data can be sent to a google sheet e.g. for summarising data for collaborators and clinicians.

1 Install the google-api-python-client

  .. code-block:: bash

      pip install --upgrade google-api-python-client

  or locally using:

  .. code-block:: bash

      pip install --upgrade google-api-python-client --user

2 Turn on Google Sheets API by following the instructions on step 1 of the `Quick start guide for python <https://developers.google.com/sheets/api/quickstart/python>`_

    - Add a new project e.g. test-api
    - Add credentials to your project (Google Sheets API, calling API from Other UI, processing user data)
    - Create an OAuth 2.0 client ID (Add you name, email address, and product name)
    - Download credentials json file (it will be called 'client_id.json' and move this file to your working directory and rename it client_secret.json

3 Run examples here: https://github.com/PrasadBabarendaGamage/google_apis
