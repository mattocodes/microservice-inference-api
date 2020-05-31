[![CircleCI](https://circleci.com/gh/mattocodes/project-ml-microservice.svg?style=svg)](https://circleci.com/gh/mattocodes/project-ml-microservice)

## Project Overview - Operationalize A Production Microservice

The goal of this project is to operationalize a machine learning Python flask app that serves out predictions about housing prices through API calls. The
project makes use of Docker and Kubernetes to containerize the Python app (app.py) to make it ready for production. 


## Setup the Environment

* Create a Python virtual environment:  `python3 -m venv ~/.project-ml-microservice` 
* Activate the virtual environment:     `source ~/.project-ml-microservice/bin/activate`
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

### List of Some Files in the Repo

* app.py - The Python flask app to operationalize
* Dockerfile - The Docker config file needed to containerize the app
* Makefile - A bash script file used to install application dependencies
* make_prediction.sh - A script file used to make predictions
* model_data - A folder containing housing data information in the Boston area
* output_txt_files - A folder containing the result of the prediction
* README.md - This file
* requirements.txt - A text file containing a list of application dependencies
* run_docker.sh - A script file used to build the Docker image
* run_kubernetes.sh - A script file used to build the Kubernetes container
* upload_docker.sh - A script file used to push the Docker image to the remote Docker repository
* .circleci - A folder that contains CircleCI's config.yml file that checks the project code for errors