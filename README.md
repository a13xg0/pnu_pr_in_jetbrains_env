# The Main idea

To demonstrate jetbrains' stack of project mangement software for my classmates I need to create not only working environment for hub, youtrack, upsource e.t.c, I need to give them abiblity to build this environment on their own laptops. 

In this case I need:
* nexus proxy, to store docker containers and other intermediate packages
* windows installer for docker
* configuration for docker to up environment
* configuration for docker to use my repository
* setup my linux laptop as a wifi AP
* nginx with file browsing. To download base config and docker

# Preparation (may be automatised in the future)

## Docker
Download the docker installation image into the dist folder

## Nexus 3
Before the demonstration we need to start configuration from docker/env folder. After successfull start and nexus 3 initialization we need to login in the sonatype nexus 3 console at 8081 port. Default user and password are admin/admin123

Theer we need to setup new docker repository proxy. 
The main repository is: https://registry-1.docker.io

More detailed instructaion can be found here:
https://help.sonatype.com/display/NXRM3/Proxy+Repository+for+Docker
https://help.sonatype.com/display/NXRM3/Realms

To access repository via proxy we need to put before docker image name an address of our docker proxy.

Secondly we need to increase TTL time for item in the cache.

## Initial system run

To obtain images in the nexus cache we need to run our jetbrains environment for the first time.
After that we can share our cahce with the other team

