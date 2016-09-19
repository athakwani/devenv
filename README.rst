This repository container dupper template for development environment.

Cloud Development Environment
=============================

You can setup development environment for any git repository using dupper by running below commands. This will start bidirectional code sync between container and local machine.

.. code-block:: bash

  # Install dupper
  curl -sSL https://get.dupper.co | sh

  # Setup Development environment
  dupper dup --name=myrepo --template-from=https://github.com/athakwani/devenv <YOUR_GIT_REPO_URL>
  dupper exec myrepo devenv <LOCAL_PATH_FOR_REPO>

You can also host development environment in Digital Ocean or any other cloud provider using docker-machine and dupper:

.. code-block:: bash
  
  # Install docker-machine
  curl -L https://github.com/docker/machine/releases/download/v0.7.0/docker-machine-`uname -s`-`uname -m` > /usr/local/bin/docker-machine 
  chmod +x /usr/local/bin/docker-machine
  
  # Provision ubuntu host with your access token 
  docker-machine create --driver digitalocean --digitalocean-access-token=<your access token> \
  --digitalocean-image "ubuntu-14-04-x64" devenv-node
  eval $(docker-machine env devenv-node)

  # Install dupper
  curl -sSL https://get.dupper.co | sh

  # Setup Development environment in devenv-node
  dupper dup --name=myrepo --template-from=https://github.com/athakwani/devenv <YOUR_GIT_REPO_URL>
  dupper exec myrepo devenv <LOCAL_PATH_FOR_REPO>
    
