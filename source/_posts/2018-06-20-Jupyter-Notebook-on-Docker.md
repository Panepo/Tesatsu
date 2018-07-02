---
title: Jupyter Notebook on Docker
categories:
  - 手札
  - 程設
tags:
  - 手札
  - 程設
date: 2018-06-20 11:37:32
---
This is the note for running jupyter notebook on docker.

Jupyter docker stacks provide several docker images, they are `base-notebook`, `minimal-notebook`, `all-spark-notebook`, `pyspark-notebook`, `scipy-notebook`, `datascience-notebook`, `tensorflow-notebook` and `r-notebook`
https://github.com/jupyter/docker-stacks

Let this post runs `base-notebook` for example:
`docker run --rm -P jupyter/base-notebook`
`--rm` means automatically remove the container when it exists. `-P` means publish all exposed ports to random ports.

Let see what is runs by inputing this command:
`docker ps`
{% codeblock %}
CONTAINER ID        IMAGE                   COMMAND                  CREATED             STATUS              PORTS                     NAMES
3464b0694c54        jupyter/base-notebook   "tini -g -- start-no…"   3 minutes ago       Up 3 minutes        0.0.0.0:32768->8888/tcp   gallant_chebyshev
{% endcodeblock %}
We can see that the port 32768 is exposed to the container port 8888, and visit `http://localhost:32768` vis browser.

The token of juypter notebook is showned on the screen, just copy it and past on the browser:
`http://localhost:32768/?token=[token]`

To fix the exposed port of container, we can replace `-P` to `-p 18888:8888`, this command will fix the exposed port to 18888.

To terminate the jupyer notebook, use `docker stop [CONTAINER ID]`

To copy files to container, use `docker cp [FILE PATH] [CONTAINER ID]:/home/jovyan/work`

### Build your docker image
To customize the docker image, a file named `Dockerfile` is needed, which contains the script to generate your customized image. Here's my example which has additional Opencv, Tensorflow and Keras installed. Besides, copy the notebook directionary to the container.
{% codeblock %}
FROM jupyter/scipy-notebook

LABEL maintainer="Panepo <panepo@github.io>"

# install tensorflow
RUN conda install --quiet --yes -c anaconda tensorflow=1.8

# install keras
RUN conda install --quiet --yes -c anaconda keras=2.2

# install opencv
RUN conda install --quiet --yes -c conda-forge opencv=3.4.1

RUN conda clean -tipsy && \
    fix-permissions $CONDA_DIR && \
    fix-permissions /home/$NB_USER

WORKDIR /app

ADD ./notebook /app
{% endcodeblock %}
Run this command to build docker image:
`docker build -t [image name] .`

### Upload your docker image to dockerhub
First, login to dockerhub
`docker login`

Then run the image you want to push
`docker run --rm [image name]`

Lunch another terminal, find the container id by this command
`docker ps`

Then commit as git
`docker commit -m "[commit message]" [container id] [repository]`

Finally, push it to dockerhub
`docker push [repository]`