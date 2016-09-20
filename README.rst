This dupper template repository is for Sync development environment.

Sync Development Environment
============================

Sync starts bidirectional code sync between repository source code and local directory. You can start sync for any git repository using below commands. 

.. code-block:: bash

  dupper dup --name=myrepo --template-from=https://github.com/athakwani/sync GITURL
  dupper exec myrepo sync DIR
      
Commands
========

* sync
    
.. code-block:: bash

    Usage:
    dupper exec CONTAINER sync DIR
    
