Welcome to XPipe's documentation !
##################################

.. image:: https://img.shields.io/badge/python-%3E%3D%203.5-blue
  
Introduction
************

Traxer allows you track your experiments parameters, metrics, artifacts and more. 

The web interface enables you to easily organize your experiments into folders, to filter them and to plot different kind of graphs. You will particularly appreciate the library if you deal with a lot of experiments.

The philosophy behind the project is to be simple and customizable.

As a team, you can run a single XPipe server for everyone. It will promote exchange as everyone can easily share their work with others.

Getting started
***************

.. code-block:: bash

  pip install traxer


Documentation (work in progress): https://traxer.readthedocs.io/en/latest/#

Experiment tracking
*******************

This feature is still experimental.

You have two options to start the server:

1. Run the server from the commandline. You must host a MongoDB server instance.

.. code-block:: bash

  traxer --db_host <db_ip_address> --db_port <db_port> --port <server_port> --artifacts-dir <artifacts_dir>

2. Run directly the docker image (no other dependancies needed)

.. code-block:: bash

  docker pull drosos/traxer:0.1.5
  docker run -v <data_dir>:/data -p <server_port>:80 drosos/traxer:0.1.5

The `<data_dir>` directory will contain the mongodb database and artifacts.

Then you can connect to http://127.0.0.1:<server_port> to access the web interface.

.. image:: https://raw.githubusercontent.com/Scotchy/Traxer/main/docs/images/gui1.png

If you open an experiment, you can get some details and results:

.. image:: https://raw.githubusercontent.com/Scotchy/Traxer/main/docs/images/gui2.png
