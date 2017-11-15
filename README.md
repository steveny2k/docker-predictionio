This project is derived from sphereio/docker-predictionio

The doc file of PredictionIO pointing to this repo is at http://predictionio.incubator.apache.org/community/projects/#docker-installation-for-predictionio

The master branch of this project is for the PredictionIO stable version 0.10.0, and other branches are for newer PredictionIO stable versions (for example, 0.12.0)

# PredictionIO docker container
Docker container for PredictionIO-based machine learning services

[![Docker build](http://dockeri.co/image/steveny/predictionio)](https://registry.hub.docker.com/u/steveny/predictionio/)

[PredictionIO](https://prediction.io) is an open-source Machine Learning
server for developers and data scientists to build and deploy predictive
applications in a fraction of the time.

This container uses Apache Spark, HBase and Elasticsearch. 

1. First, do either a) or b) below

    a). (faster; stable version) obtain docker image from public docker registry:

    ```Bash
    $ docker run -it -p 8000:8000 steveny/predictionio /bin/bash
    ```
    
    b). (slower) build docker image from local Dockerfile: git checkout the desired branch; cd to the path containing the Dockerfile, then:
    
    ```Bash
    $ docker build -t predictionio .
    ```
    then:
    
    ```Bash
    $ docker run -p 8000:8000 --name predictionio_instance -it predictionio /bin/bash
    ```
    
2. Then in docker container, start all services 
  ```Bash
  $ pio-start-all
  or 
  $ pio eventserver &  # if using PostgreSQL or MySQL
  ```
   and check if they are started
  ```Bash
  $ jps -l
  ```

3. Try an example: similar Product Engine Template (details in http://predictionio.incubator.apache.org/templates/similarproduct/quickstart/)
   
=========================

Note to myself:

command lines to build and push docker image:
```Bash
$ docker build -t steveny/predictionio:0.12.0 .
$ docker run --rm -it -p 8000:8000 steveny/predictionio:0.12.0 /bin/bash
$ docker push steveny/predictionio:0.12.0
```


