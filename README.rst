#################################
Welcome to the Clickpecker Bundle
#################################

Introduction
============

This bundle allows you to launch the latest stable version of Clickpecker.

Content:
    * Clickpecker library (`repo <https://github.com/VladX09/clickpecker-library>`_)(`docs <http://clickpecker-library.readthedocs.io/en/latest/>`_)
    * Clickpecker device manager (`repo <https://github.com/VladX09/clickpecker-device-manager>`_)(`docs <http://clickpecker-device-manager.readthedocs.io/en/latest/>`_)
    * Clickpecker pytest plugin (`repo <https://github.com/VladX09/clickpecker-pytest>`_)

Launching
=========

All the system and it's requirements is provided in docker containers.
You will need ``docker`` and ``docker-compose`` to build and launch it.
Run::

 docker-compose up -d --build

After building the images you will get two containers:
    * ``device_manager`` - contains running *clickpecker-device-manager* server. It is accessible from ``127.0.0.1/5000``.
    * ``pytest_worker`` - container to run your tests. Default working directory contains ``clickpecker-pytest/examples/``, you can change this in docker-compose.yml

To launch your tests in the worker, run::

  docker exec pytest_worker pytest [...]

(Be sure, that containers are running)
