..
    This file is part of GEO Knowledge Hub.
    Copyright 2020 GEO Secretariat.

    GEO Knowledge Hub is free software; you can redistribute it and/or modify it
    under the terms of the MIT License; see LICENSE file for more details.


Install GEO Knowledge Hub Digital Library
=========================================


``GEO Knowledge Hub`` depends essentially on `InvenioRDM <https://invenio-software.org/products/rdm/>`_. Please, read the instructions below in order to install ``GEO Knowledge Hub``.


Development installation
------------------------


Pre-Requirements
++++++++++++++++


- `Python <https://www.python.org/>`_ 3.7+

- `nodejs <https://nodejs.org/>`_ 13.0.0+

- `Docker <https://docs.docker.com/>`_ 1.13.0+

- `Docker-Compose <https://docs.docker.com/>`_ 1.17.0+


.. note::

    The Anaconda Python version is not currently supported by InvenioRDM. Please, for more details, refer to the section `Pre-Requirements <https://inveniordm.docs.cern.ch/install/#pre-requirements>`_ in InvenioRDM documentation.


Clone the software repository
+++++++++++++++++++++++++++++


Use ``git`` to clone the software repository::

    git clone https://github.com/geo-knowledge-hub/geo-knowledge-hub.git


Go to the source code folder::

    cd geo-knowledge-hub


Install the Invenio-CLI
+++++++++++++++++++++++


Via pip::

    pip install invenio-cli


Check the installed version::

    invenio-cli --version


.. note::

    You can use your favorite way to install a Python package. Please, refer to the section `Install the CLI <https://inveniordm.docs.cern.ch/install/#install-the-cli>`_ in the InvenioRDM documentation.


.. note::

    If you want to create a new Python Virtual Environment, please, follow this instruction:

    *1.* Create a new virtual environment linked to Python 3.7::

        python3.7 -m venv venv


    **2.** Activate the new environment::

        source venv/bin/activate


    **3.** Update pip and setuptools::

        pip3 install --upgrade pip

        pip3 install --upgrade setuptools


.. note::

    We are using ``invenio-cli`` version 0.14.2.


Local Installation
++++++++++++++++++


We will run GEO Knowledge Hub locally and the database and other services in Docker containers.


From the GEO Knowledge Hub folder, install all the dependencies with the help of ``invenio-cli``::

    invenio-cli install --pre


After installing all the dependency libraries, setup the PostgreSQL, Elasticsearch, Redis and RabbitMQ containers::

    invenio-cli services --force


Run GEO Knowledge Hub
+++++++++++++++++++++


After installing locally and preparing the services, start GEO Knowledge Hub::

    invenio-cli run


If everything went well, you can open your browser and point to the following address::

    firefox https://localhost:5000


Production installation
-----------------------


**Under Development**
