cloud-helloworld
================

Hello World demo project for SAP HANA Cloud Platform https://account.hanatrial.ondemand.com

This hello world sample is based on the hello sample that you find in the SDK. The SDK is 
provided under the SAP DEVELOPER LICENSE AGREEMENT that you find at 
https://tools.hana.ondemand.com/developer-license-3.1.txt

Changes compared to original sample:
- use standard Maven layout
- don't submit Eclipse files to git

For general information regarding SDK samples see SAP_CLOUD_SDK/samples/readme.txt

# Building 

Needed environment variables for build:
- PROXY_HOST, PROXY_PORT, SAP_CLOUD_ACCOUNT, SAP_CLOUD_USERNAME SAP_CLOUD_PASSWORD for 
  running integration test in the cloud

Build the project and run unit tests:
mvn clean package

Run integration tests on local runtime:
mvn clean verify -P local-integration-tests

Run integration test in cloud:
mvn verify -P cloud-integration-tests

# Importing project to Eclipse

Prerequisites:
- SAP HANA Cloud Tools: https://tools.hana.ondemand.com/#cloud
- M2Eclipse (with WTP extension)

Import the project as 'Existing Maven Project': File -> Import... -> Maven -> Existing Maven Projects

# Building with Jenkins

- [CI Job](https://jenkinsp1940131088trial.hanatrial.ondemand.com/job/cloud-hello-world/) - builds the project and runs the integration tests in cloud

For more information about running Jenkins on Jenkins on SAP HANA Cloud Platform, you can read the following [Blog: Run your own Jenkins on SAP HANA Cloud Platform](http://scn.sap.com/community/developer-center/cloud-platform/blog/2013/10/11/run-your-own-jenkins-on-sap-hana-cloud-platform) and have a look at 
https://github.com/SAP/cloud-jenkins.

