This repository contains dupper template for Sync development environment.

Sync Development Environment
=============================

You can setup development environment for any git repository using dupper by running below commands. This will start bidirectional code sync between container and local machine.

.. code-block:: bash

  dupper dup --name=myrepo --template-from=https://github.com/athakwani/sync <YOUR_GIT_REPO_URL>
  dupper exec myrepo sync <LOCAL_PATH_FOR_REPO>
  
Dependencies
============

    * curl
    * sudo
    * inotify-tools
    * openssh-server
    * `gut <https://github.com/tillberg/gut>`_
    
Implements
==========

    * sync
    
.. code-block:: bash

    Usage:
    dupper exec CONTAINER sync LOCALPATH
    
