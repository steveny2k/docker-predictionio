This project is derived from sphereio/docker-predictionio

The doc file of PredictionIO pointing to this repo is at http://predictionio.incubator.apache.org/community/projects/#docker-installation-for-predictionio

This Dockerfile is for PredictionIO v0.10.0

# PredictionIO docker container
Docker container for PredictionIO-based machine learning services

[![Docker build](http://dockeri.co/image/steveny/predictionio)](https://registry.hub.docker.com/u/steveny/predictionio/)

[PredictionIO](https://prediction.io) is an open-source Machine Learning
server for developers and data scientists to build and deploy predictive
applications in a fraction of the time.

This container uses Apache Spark, HBase and Elasticsearch. The PredictionIO version is the latest stable version 0.10.0.

####Use it interactively for development:
1. First, do either i) or ii) below
  1. (faster; stable version) obtain docker image from public docker registry:

    ```Bash
    $ docker run -it -p 8000:8000 steveny/predictionio /bin/bash
    ```
  2. (slower) build docker image from local Dockerfile: cd to the path containing the Dockerfile, then:
    
    ```Bash
    $ docker build -t predictionio .
    ```
    then:
    
    ```Bash
    $ docker run -p 8000:8000 --name predictionio_instance -it predictionio /bin/bash
    ```
    
2. Then in docker container, start all services and check they are started
  ```Bash
  $ pio-start-all
  or 
  $ pio eventserver &  # if using PostgreSQL or MySQL
  $
  $ jps -l
  ```

3. Try an example: similar Product Engine Template (details in http://predictionio.incubator.apache.org/templates/similarproduct/quickstart/)
   



