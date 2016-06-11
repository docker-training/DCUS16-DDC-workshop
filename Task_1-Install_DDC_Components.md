# Task 1: Install Docker Datacenter Components

In this task you will install the various components of Docker Datacenter. Here is an overview:

1. Install Commercially Supported Docker Engine (CS Engine)
2. Install Docker Universal Control Plane (UCP)
3. Install Docker Trusted Registry (DTR)
4. Verify LDAP Server

## Prerequisites
- 4 Linux-based Host VMs (2 for UCP, 1 for DTR, 1 for pre-configured LDAP server)

## Install CS Docker Engine

In this step you will install CS Engine on the three hosts used for UCP and DTR. Note that you do not need to install CS Engine on the node with the pre-configured LDAP server.

1. Verify that you can log into the terminal command line interface for each of the three hosts.

2. Follow these instructions to install CS Engine on each of the 3 hosts: https://docs.docker.com/docker-trusted-registry/cs-engine/install/

  - Follow the instructions for installing on Ubuntu 14.04 LTS.

3. Confirm that the Docker CS Engine is installed by running `sudo docker info` on each host.

## Install Universal Control Plane

In this step you will install UCP on your first two hosts. You will install a UCP Controller on the first host and join a UCP node on the second host. 

1. Follow the instructions here to install UCP: https://docs.docker.com/ucp/installation/install-production/

  - Log into your first host to install a UCP controller. Log into your second host to join a UCP node (non-replica) to the cluster.
  - You can skip all steps labeled optional (steps 3, 4, 7, 8). This tutorial is not a high-availability install.
  - Use the license file provided by your instructors when installing UCP.

2. Verify UCP is functioning by logging into UCP as an admin.

## Install Docker Trusted Registry

In this step you will install DTR on your third host. DTR requires a UCP cluster to be deployed beforehand for orchestration purposes.

1. Log into your third host. Follow the instructions here to install DTR: https://docs.docker.com/docker-trusted-registry/install/install-dtr/

  - You can skip all steps labeled optional (step 6). This tutorial is not a high-availability install.
  - Use the license file provided by your instructors when installing DTR.
  
2. Verify DTR is functioning by logging into DTR as an admin.

## Verify LDAP Server

The fourth host provided for you contains an LDAP server, to be used in a later task. 

1. Verify that this host exists and that you can log into its terminal command line interface.

You should now have CS Engine, UCP, and DTR installed, and be ready to move on to the next task.
