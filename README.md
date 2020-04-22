# Node Cookbook :monkey: :cyclone:
This repository contains Nodejs and by following the steps below you will be able to install Nodejs using the cookbook.

Chef is a configuration management tool for automating machine which are setup on physical servers, virtual machines and in the cloud. Configuration management is all about trying to ensure that the files and software you are expecting to be on a machine are present, configured correctly, and working as intended.
#### Benefits of Chef
- Accelerating software delivery
- Increased service Resiliency
- Risk Management
- Cloud Adoption
- Infrastructure agnostic

### Pre-requisites

- Chef
- NodeJs
- Nginx
- pm2 and npm
- Git
- Virtual Box

## Steps
The steps below will show you how to run this cookbook, please ensure you cloned the repo and navigate to your folder called 'NodeCookbookStarterCode' within your terminal.

After you have done that, please follow the commands below.

##### Test locally
We will test locally first to ensure that all the tests pass, to do this run the unit tests:
```
$ chef exec rspec
```
Now locally run the integration tests and close machine:
```
$ kitchen test
```
##### Test in AWS
Now that all our test have passed, we will run the integration test in AWS:
```
KITCHEN_YAML=.kitchen_cloud.yml kitchen test
```

If you fail to connect to AWS or having any issues, this maybe due to the 'subnet_id' or 'region'.
The 'subnet_id' can cause issues if you are using the incorrect subnet, so change the subnet_id to your subnet.

Also the 'region' maybe cause your connection to be slow if you are connecting to region that is far from you, so change this to a region that is closer to you.
