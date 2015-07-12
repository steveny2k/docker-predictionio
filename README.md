# PredictionIO docker container
Docker container for PredictionIO-based machine learning services

[![Docker build](http://dockeri.co/image/sphereio/predictionio)](https://registry.hub.docker.com/u/sphereio/predictionio/)

[PredictionIO](https://prediction.io) is an open-source Machine Learning
server for developers and data scientists to build and deploy predictive
applications in a fraction of the time.

This container uses Apache Spark, HBase and Elasticsearch.
Use it interactively for development:

```Bash
$ docker run -it -v $HOME/MyEngine:/MyEngine sphereio/predictionio /bin/bash
```

Or create your own deployable docker container:

```Dockerfile
FROM sphereio/predictionio

ADD MyEngine /MyEngine

EXPOSE 8000

ADD run.sh /run.sh

ENTRYPOINT /run.sh
```

and run.sh:

```Bash
#!/bin/bash

set -e

pio-start-all
cd /MyEngine
pio build --verbose
pio deploy
```
