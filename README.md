# gradle-mvn-push

A gradle script for deploying to MavenCentral using Sonatype and Nexus

## Required properties (usually found in gradle.properties):
- ```VERSION_NAME=<the version name - eg 0.1>```
- ```GROUP=<the maven group - eg com.staticbloc>```
- ```POM_NAME=<the artifact name - eg Jobs>```
- ```POM_ARTIFACT_ID=<the artifact id, will be used as the artifact filename - eg jobs>```
- ```POM_PACKAGING=<the artifact type - eg aar>```
- ```POM_DESCRIPTION=<the artifact description - A task queue library for Android.>```
- ```POM_URL=<the artifact's source URL - eg https://github.com/eygraber/jobs>```
- ```POM_SCM_URL=<the artifact's source URL - eg https://github.com/eygraber/jobs>```
- ```POM_SCM_CONNECTION=<the artifact's source URL - eg scm:git@github.com:eygraber/jobs.git>```
- ```POM_SCM_DEV_CONNECTION=<the artifact's source URL - eg scm:git@github.com:eygraber/jobs.git>```
- ```POM_LICENCE_NAME=<the artifact's license name - eg The Apache Software License, Version 2.0>```
- ```POM_LICENCE_URL=<the artifact's license URL - eg http://www.apache.org/licenses/LICENSE-2.0.txt>```
- ```POM_LICENCE_DIST=<the artifact's dist - eg repo>```
- ```POM_DEVELOPER_ID=<the id of the developer - eg eygraber>```
- ```POM_DEVELOPER_NAME=<the name of the developer - eg Eliezer Graber>```

## The following properties are optional:
- ```PGP_KEY_ID=<pgp key ID>```
- ```PGP_SECRET_KEY_RING=<absolute path to pgp secring.gpg file>```
- ```PGP_PRIVATE_KEY_PASSWORD=<password for pgp private key>```
- ```NEXUS_USERNAME=<username for nexus/sonatype account>```
- ```NEXUS_PASSWORD=<password for nexus/sonatype account>```
    
This script should be included in build.gradle like so:
        
        apply from: 'https://raw.githubusercontent.com/eygraber/gradle-mvn-push/master/gradle-mvn-push.gradle'
