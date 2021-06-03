[![Build Status](https://travis-ci.org/mborges-pivotal/pcf-ers-demo1.svg?branch=master)](https://travis-ci.org/mborges-pivotal/pcf-ers-demo1)
[ ![Download](https://api.bintray.com/packages/mborges-pivotal/generic/pcf-ers-demo1/images/download.svg) ](https://bintray.com/mborges-pivotal/generic/pcf-ers-demo1/_latestVersion)

# VMware Tanzu Application Service (TAS) Base Demo
Base application to demonstrate VMware TAS.

## Credits and contributions
* Andrew Ripka's [cf-workshop-spring-boot github repo](https://github.com/pivotal-cf-workshop/cf-workshop-spring-boot)
* Marcelo Borges's [pcf-ers github repo](https://github.com/Tanzu-Field-Engineering/pcf-ers-demo)

## Introduction
This base application is intended to demonstrate some of the basic functionality of VMware TAS:

* TAS api, target, login, and push
* TAS environment variables
  * Spring Cloud Profiles
* Scaling, self-healing, router and load balancing
* RDBMS service and application auto-configuration
* Blue green deployments

## Getting Started

**Prerequisites**
- [Cloud Foundry CLI](https://network.pivotal.io/products/elastic-runtime)
- [Git Client](http://info.pivotal.io/i1RI0AUe6gN00C010l12J0R)
- An IDE, like [Spring Tool Suite](http://info.pivotal.io/f00RC0N0lh01eU21IAJ260R)
- [Java SE Development Kit](http://info.pivotal.io/n0I60i3021AN0JU0le10CRR)

**Building**
```
$ git clone [REPO]
$ cd [REPO]
$ ./mvnw clean install
```

### To run the application locally
The application is set to use an embedded H2 database in non-PaaS environments, and to take advantage of Tanzu CF's auto-configuration for services. To use a MySQL Dev service in TAS, simply create and bind a service to the app and restart the app. No additional configuration is necessary when running locally or in Tanzu CF.

In Tanzu CF, it is assumed that a Tanzu MySQL service will be used.

```
$ ./mvnw spring-boot:run
```

Then go to the http://localhost:8080 in your browser

### Running on Cloud Foundry
Take a look at the manifest file for the recommended setting. Adjust them as per your environment.

## Labs/Demo Scripts summary
We have a [Labs](https://github.com/dbuchko/pcf101-workshop/tree/master/Labs) folder to help you learn TAS. These labs can be used for workshops or self-training.    
