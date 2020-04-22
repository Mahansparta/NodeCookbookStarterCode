# Node Cookbook

Description


## list of what installs
- NodeJs
- Nginx
- pm2 and npm


## Commands

### test locally

Running my unit test:
```
chef exec rspec
```

running integration tests and closing machine:
```
kitchen test
```

### test in AWS

Running integration tests in AWS
```
KITCHEN_YAML=kitchen_cloud.yml kitchen test
```
