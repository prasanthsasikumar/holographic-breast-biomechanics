===========
Online IDEs
===========
Alternative IDE are available that can be run entirely in the Cloud.

.. note::
   If your team requires you to use in-house software as part of your projects then it may not be possible to access and build that software on cloud-based IDEs.

Google Colab
------------
`Google Colaboratory <https://colab.research.google.com/>`_ or “Colab” for short is a **free** Python Jupyter notebook environment from Google Research that runs entirely in the cloud. There is no setup process. The notebooks that you create can be simultaneously edited by you and your collaborators — similar to how you can collaboratively edit documents in Google Docs. It is especially well suited to machine learning, data analysis and education and **provides free access to computing resources including GPUs (Nvidia K80s, T4s, P4s and P100s)**.

  .. figure:: google_colab_ide.png
    :width: 700
    :align: center
    :figclass: align-center

    Google Colab IDE.

Navigate to https://colab.research.google.com to get started. See the `Colab FAQ <https://research.google.com/colaboratory/faq.html>`_ for more information on usage limits of the free GPUs provided by this service.

Binder
------
The `Binder Project <https://mybinder.org/>`_ allow you to package and share interactive, reproducible environments. A Binder or "Binder-ready repository" is a code repository that contains both code and content to run, and configuration files for the environment needed to run it.

This allows you to take a code repository e.g .on Github that may contain Jupyter notebooks, and open those notebooks in an executable environment, making your code immediately reproducible by anyone, anywhere.

  .. figure:: mybinder.png
    :width: 700
    :align: center
    :figclass: align-center

    Binder setup page.

Binderhub
~~~~~~~~~
A BinderHub lets you launch a publicly executable version of a Binder repository. Given a URL to a repository, it generates a new URL that anyone can visit in a browser to interact with a running version of the code in that repository.