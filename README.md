
# PredictionIO docker container
Docker container for PredictionIO-based machine learning services

[![Docker build](http://dockeri.co/image/sphereio/predictionio)](https://registry.hub.docker.com/u/sphereio/predictionio/)

[PredictionIO](https://prediction.io) is an open-source Machine Learning
server for developers and data scientists to build and deploy predictive
applications in a fraction of the time.

This container uses Apache Spark, HBase and Elasticsearch.

####Use it interactively for development:
First, do either A) or B)
A) obtain docker image from public docker registry:

```Bash
$ docker run -it -v $HOME/MyEngine:/MyEngine -p 8000:8000 sphereio/predictionio /bin/bash
```

or
B) build docker image from local Dockerfile:
cd to the path containing the Dockerfile, then:
```Bash
$ docker build -t predictionio .
```
then:
```Bash
$ docker run -name predictionio_instance -it predictionio
```

After finishing either A) or B) above,
Then in container 
```Bash
$ pio-start-all
$ pio status
```



