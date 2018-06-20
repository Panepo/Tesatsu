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