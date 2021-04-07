# Cloud Foundry

This demonstrates how to run the Business Events application in Cloud foundry.

## Prerequisites
* Install Ops Manager on available Iaas platforms referring Ops Manager [https://docs.pivotal.io/ops-manager/2-10/install/index.html].
* Install the Small footprint Tanzu Application Service(TAS) using here[https://docs.pivotal.io/application-service/2-10/operating/configure-pas.html].
* Install the cf cli[https://docs.pivotal.io/application-service/2-10/cf-cli/install-go-cli.html].

## Cf setup

1)Login to the cloud foundry using the below command:

cf login -a API-URL -u USERNAME -p PASSWORD

-API-URL is your API endpoint, the URL of the Cloud Controller in your TAS for VMs instance.
-USERNAME and PASSWORD are the Admin credentials in UAA section from Small footprint TAS tile Credentials tab.

2)Target a specific organization and space. 
cf target -o ORG -s SPACE

-ORG is the org you want to target.
-SPACE is the space you want to target.
Note: Required organizations and spaces can be created using the cf commands

3)Enable the diego-docker feature to run docker images. 
cf enable-feature-flag diego_docker

## Deploying BE application

