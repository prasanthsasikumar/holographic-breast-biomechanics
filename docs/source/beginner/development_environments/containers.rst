We have setup a container-based development environment to help researchers develop software for their projects. This development environment includes commonly used IDEs including PyCharm, Visual Studio Code, and JupyterLab. This provides a replicable sandboxed environment for you to develop your software.

The objectives of this tutorial are to familiarise yourself with:

- setting up the container-based development-environment;

- running IDEs from within the development-environment;

- how to install additional dependencies that your program may require (e.g. third-party python libraries); and

- how to develop your software project within the development-environment.

.. toctree::
   :maxdepth: 2

   containers/introduction
   containers/install
   containers/running
   containers/installing_dependencies
   containers/setting_up_projects
   containers/faq

.. seealso::

  The development-environment we have implemented is based on the Jupyter Stacks "base-notebook" and "scipy-notebook" Docker images. Briefly, when the development-environment Docker image is run, it creates a Linux container with a single unprivileged user called "jovyan" whom you can use to interact with the container. Through this user, you will have ownership over the "/home/jovyan" folder within the container. We can access files on our host operating system from within a running development-environment container by mounting folders within "/home/jovyan". More information on the configuration of this user can be found on the `Jupyter Docker Stacks documentation <https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html>`_.


