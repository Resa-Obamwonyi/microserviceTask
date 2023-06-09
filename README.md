[![CircleCI](https://dl.circleci.com/status-badge/img/gh/Resa-Obamwonyi/microserviceTask/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/Resa-Obamwonyi/microserviceTask/tree/main)
## Introduction

In this project, I applied the skills I have acquired in this course to operationalize a Machine Learning Microservice API. 

I was given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

## Project Motivation

To practicalize all of the techniques and methods taught in the "Microservices at scale, using AWS and Kubernetes" module
## Project Goal

The project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. 

## Tech Stack
- Python
- Flask
- Kubernetes
- Docker
- Pylint
- Hadolint
- CircleCI

## Tasks
In this project I:
* Tested the project code using linting
* Completed a Dockerfile to containerize this application
* Deployed the containerized application using Docker and made a prediction
* Improved the log statements in the source code for this application
* Configured Kubernetes and created a Kubernetes cluster
* Deployed a container using Kubernetes and made a prediction
* Uploaded a complete Github repo with CircleCI to indicate that the code has been tested

## How to Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies
* Run `make lint` to check for linting errors

## Running in Docker

Run `./run_docker.sh` to start the docker container, and create the flask app within the container, then run `./make_prediction.sh` to make predictions

## Running in Kubernetes Cluster

Install minikube and virtualbox, then run `minikube start` to start a local cluster 
Run `./run_kubernetes.sh` to start the kubernetes pod and create the flask app in the container, then run `./make_prediction.sh` to make predictions, run_kubernetes.sh contains kubectl commands for running the container with kubernetes
