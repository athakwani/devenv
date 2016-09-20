This repository contains `dupper <https://github.com/athakwani/dupper>`_ template for Sync development environment.

Sync Development Environment
=============================

Sync starts bidirectional code between between dupper container and local machine. You can start development environment for any git repository using dupper by running below commands. 

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
    
Commands
========

    * sync
    
.. code-block:: bash

    Usage:
    dupper exec CONTAINER sync LOCALPATH
    
