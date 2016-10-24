This project is tested on OSX 10.11.6

  (project is derived from sphereio/docker-predictionio)

# PredictionIO docker container
Docker container for PredictionIO-based machine learning services

(to modify)
[![Docker build](http://dockeri.co/image/sphereio/predictionio)](https://registry.hub.docker.com/u/sphereio/predictionio/)

[PredictionIO](https://prediction.io) is an open-source Machine Learning
server for developers and data scientists to build and deploy predictive
applications in a fraction of the time.

This container uses Apache Spark, HBase and Elasticsearch.

####Use it interactively for development:
1. First, do either i) or ii) below
  1. (faster; but may be outdated) obtain docker image from public docker registry:

    ```Bash
    $ docker run -it -v $HOME/MyEngine:/MyEngine -p 8000:8000 sphereio/predictionio /bin/bash
    ```
  2. (slower) build docker image from local Dockerfile: cd to the path containing the Dockerfile, then:
    
    ```Bash
    $ docker build -t predictionio .
    ```
    then:
    
    ```Bash
    $ docker run -p 8000:8000 --name predictionio_instance -it predictionio
    ```

2. Try examples
  1. Similar Product Engine Template (details in http://predictionio.incubator.apache.org/templates/similarproduct/quickstart/)
    1. 



