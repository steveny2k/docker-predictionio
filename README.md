
# PredictionIO docker container
Docker container for PredictionIO-based machine learning services

[![Docker build](http://dockeri.co/image/sphereio/predictionio)](https://registry.hub.docker.com/u/sphereio/predictionio/)

[PredictionIO](https://prediction.io) is an open-source Machine Learning
server for developers and data scientists to build and deploy predictive
applications in a fraction of the time.

This container uses Apache Spark, HBase and Elasticsearch.

####Use it interactively for development:
1. First, do either i) or ii) below
  1. obtain docker image from public docker registry:

    ```Bash
    $ docker run -it -v $HOME/MyEngine:/MyEngine -p 8000:8000 sphereio/predictionio /bin/bash
    ```
  2. build docker image from local Dockerfile: cd to the path containing the Dockerfile, then:
    
    ```Bash
    $ docker build -t predictionio .
    ```
    then:
    
    ```Bash
    $ docker run -name predictionio_instance -it predictionio
    ```

2. After finishing either i) or ii) above,
  then in container 
  ```Bash
  $ pio-start-all
  $ pio status
  ```



