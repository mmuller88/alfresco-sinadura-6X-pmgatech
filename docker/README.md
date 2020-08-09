# Alfresco Sinadura 6.2 Project

This project is originated from https://github.com/zylklab/alfresco-sinadura . So please go there for specific Sinadura matters.

I would like to thank [PMGA.tech](http://www.pmga.tech/) as my sponsor to make the work possible. 

It is planned to contribute back to the origin. But until then I would like to thank the creators of the Alfresco Sinadura addon for this sophisticated product.

## SDK

This project is based on Alfresco's SDK 4.1.0 to make it ACS 6.X compatible. For more details on how the SDK works visit: https://github.com/Alfresco/alfresco-sdk

## Useful Commands

Run with `./run.sh build_start` or `./run.bat build_start` and verify that it

 * Runs Alfresco Content Service (ACS)
 * Runs Alfresco Share
 * Runs Alfresco Search Service (ASS)
 * Runs PostgreSQL database
 * Deploys the JAR assembled modules
 
All the services of the project are now run as docker containers. The run script offers the next tasks:

 * `build_start`. Build the whole project, recreate the ACS and Share docker images, start the dockerised environment composed by ACS, Share, ASS and 
 PostgreSQL and tail the logs of all the containers.
 * `build_start_it_supported`. Build the whole project including dependencies required for IT execution, recreate the ACS and Share docker images, start the 
 dockerised environment composed by ACS, Share, ASS and PostgreSQL and tail the logs of all the containers.
 * `start`. Start the dockerised environment without building the project and tail the logs of all the containers.
 * `stop`. Stop the dockerised environment.
 * `purge`. Stop the dockerised container and delete all the persistent data (docker volumes).
 * `tail`. Tail the logs of all the containers.
 * `reload_share`. Build the Share module, recreate the Share docker image and restart the Share container.
 * `reload_acs`. Build the ACS module, recreate the ACS docker image and restart the ACS container.
 * `build_test`. Build the whole project, recreate the ACS and Share docker images, start the dockerised environment, execute the integration tests from the
 `integration-tests` module and stop the environment.
 * `test`. Execute the integration tests (the environment must be already started).

## Notice
* The Share image applies the fix for allowing the signature in the preview. https://github.com/zylklab/alfresco-sinadura/issues/9