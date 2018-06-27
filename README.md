siddhi-store-mongodb
======================================

The **siddhi-store-mongodb extension** is an extension to <a target="_blank" href="https://wso2.github.io/siddhi">Siddhi</a> that  can be used to persist events to a MongoDB instance of the users choice.
Find some useful links below:

* <a target="_blank" href="https://github.com/wso2-extensions/siddhi-store-mongodb">Source code</a>
* <a target="_blank" href="https://github.com/wso2-extensions/siddhi-store-mongodb/releases">Releases</a>
* <a target="_blank" href="https://github.com/wso2-extensions/siddhi-store-mongodb/issues">Issue tracker</a>

## Latest API Docs 

Latest API Docs is <a target="_blank" href="https://wso2-extensions.github.io/siddhi-store-mongodb/api/1.0.14">1.0.14</a>.

## Prerequisites

 * A MongoDB server instance should be started.
 * User should have the necessary privileges and access rights to connect to the MongoDB data store of choice.

## How to use 

**Using the extension in <a target="_blank" href="https://github.com/wso2/product-sp">WSO2 Stream Processor</a>**

* You can use this extension in the latest <a target="_blank" href="https://github.com/wso2/product-sp/releases">WSO2 Stream Processor</a> that is a part of <a target="_blank" href="http://wso2.com/analytics?utm_source=gitanalytics&utm_campaign=gitanalytics_Jul17">WSO2 Analytics</a> offering, with editor, debugger and simulation support. 

* This extension is shipped by default with WSO2 Stream Processor, if you wish to use an alternative version of this extension you can replace the component <a target="_blank" href="https://github.com/wso2-extensions/siddhi-store-mongodb/releases">jar</a> that can be found in the `<STREAM_PROCESSOR_HOME>/lib` directory.

**Using the extension as a <a target="_blank" href="https://wso2.github.io/siddhi/documentation/running-as-a-java-library">java library</a>**

* This extension can be added as a maven dependency along with other Siddhi dependencies to your project.

```
     <dependency>
        <groupId>org.wso2.extension.siddhi.store.mongodb</groupId>
        <artifactId>siddhi-store-mongodb</artifactId>
        <version>x.x.x</version>
     </dependency>
```

## Running Integration tests in docker containers(Optional)

The MongoDB functionality are tested with the docker base integration test framework. The test framework initializes the docker container according to the given profile before executing the test suite.

1. Install and run docker in daemon mode.

    *  Installing docker on Linux,<br>
       Note:<br>    These commands retrieve content from get.docker.com web in a quiet output-document mode and install.Then we need to stop docker service as it needs to restart docker in daemon mode. After that, we need to export docker daemon host.
       
        > wget -qO- https://get.docker.com/ | sh
        >
        > sudo service dockerd stop
        >
        > export DOCKER_HOST=tcp://172.17.0.1:4326
        >
        > docker daemon -H tcp://172.17.0.1:4326

    *  On installing docker on Mac, see <a target="_blank" href="https://docs.docker.com/docker-for-mac/">Get started with Docker for Mac</a>

    *  On installing docker on Windows, see <a target="_blank" href="https://docs.docker.com/docker-for-windows/">Get started with Docker for Windows</a>
   
2. To run the integration tests, issue the following commands.

    * MongoDB without SSL connection
    
           ```
           mvn verify -P mongod -Ddocker.removeVolumes=true
           ```

    * MongoDB with SSL connection
           
           ```
           mvn verify -P mongod-ssl -Ddocker.removeVolumes=true
           ```
           
## Jenkins Build Status

---

|  Branch | Build Status |
| :------ |:------------ | 
| master  | [![Build Status](https://wso2.org/jenkins/job/siddhi/job/siddhi-store-mongodb/badge/icon)](https://wso2.org/jenkins/job/siddhi/job/siddhi-store-mongodb/) |

---

## Features

* <a target="_blank" href="https://wso2-extensions.github.io/siddhi-store-mongodb/api/1.0.14/#mongodb-store">mongodb</a> *<a target="_blank" href="https://wso2.github.io/siddhi/documentation/siddhi-4.0/#store">(Store)</a>*<br><div style="padding-left: 1em;"><p>Using this extension a MongoDB Event Table can be configured to persist events in a MongoDB of user's choice.</p></div>

## How to Contribute
 
  * Please report issues at <a target="_blank" href="https://github.com/wso2-extensions/siddhi-store-mongodb/issues">GitHub Issue Tracker</a>.
  
  * Send your contributions as pull requests to <a target="_blank" href="https://github.com/wso2-extensions/siddhi-store-mongodb/tree/master">master branch</a>. 
 
## Contact us 

 * Post your questions with the <a target="_blank" href="http://stackoverflow.com/search?q=siddhi">"Siddhi"</a> tag in <a target="_blank" href="http://stackoverflow.com/search?q=siddhi">Stackoverflow</a>. 
 
 * Siddhi developers can be contacted via the mailing lists:
 
    Developers List   : [dev@wso2.org](mailto:dev@wso2.org)
    
    Architecture List : [architecture@wso2.org](mailto:architecture@wso2.org)
 
## Support 

* We are committed to ensuring support for this extension in production. Our unique approach ensures that all support leverages our open development methodology and is provided by the very same engineers who build the technology. 

* For more details and to take advantage of this unique opportunity contact us via <a target="_blank" href="http://wso2.com/support?utm_source=gitanalytics&utm_campaign=gitanalytics_Jul17">http://wso2.com/support/</a>. 
