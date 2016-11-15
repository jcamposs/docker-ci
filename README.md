# Docker Continuous Integration

This image contains a Jenkins and a Sonar installation

* Jenkins 1.647 with plugins:
   * git
   * git-client
   * scm-api
   * build-pipeline-plugin
   * parameterized-trigger
   * jquery
   * conditional-buildstep
   * run-condition
   * token-macro
   * copyartifact
   * promoted-builds
   * groovy-postbuild


* Sonar 5.3_all
   * sonar-javascript-plugin-2.10
   * sonar-groovy-plugin-1.3.1
   * sonar-scalastyle-plugin-0.0.1-SNAPSHOT

* Java 1.8
* Node
* Gulp
* Grunt
* Bower
* PhantomJS
* Meteor 1.4
* Heroku Toolbelt


# Some useful commands:

    # Build the image
    $ docker build --tag="jcamposs/docker-ci" .

    # Run a container
    $ docker docker run -d \
          -p 8888:8080 \
          -p 9000:9000 \
          -p 9092:9092 \
          --name="ci" \
          jcamposs/docker-ci

    # Attach to the container
    $ docker exec -i -t ci /bin/bash

    # Stop the container
    $ docker stop ci

    # Re-start the container
    $ docker start ci

    # remove the container
    $ docker rm ci

    # remove the image
    $ docker rmi jcamposs/docker-ci


## Usage
* Browse to Jenkins : [http://localhost:8888](http://localhost:8888)
* Browse to Sonar : [http://localhost:9000](http://localhost:9000)
* Sonar DB : jdbc:h2:tcp://localhost:9092/sonar
