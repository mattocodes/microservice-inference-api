[![CircleCI](https://circleci.com/gh/mattocodes/microservice-inference-api.svg?style=svg)](https://circleci.com/gh/mattocodes/microservice-inference-api)

# Operationalize a Production Microservice

This project is about operationalizing a machine learning microservice 
inference API app using Docker, Kubernetes, and CircleCI. The microservice app is a Flask based app that serves out predictions or inferences about housing prices through API calls. Furthermore, the app uses an [`sklearn`](https://scikit-learn.org/) machine learning training model. 
 

## Environment Setup

* Create a Python virtual environment: 

    ```
        $ python3 -m venv ~/.microservice-inference-api
    ```

* Activate the virtual environment: 

    ```
        $ source ~/.microservice-inference-api/bin/activate
    ```

* Run `make install` to install the necessary dependencies:

    ```
        $ make install
    ```

### Running `app.py`

1. Standalone: 

    ```
        $ python app.py
    ```

2. Run in Docker: 

    ```
        $ ./run_docker.sh
    ```

3. Run in Kubernetes: 

    ```
        $ ./run_kubernetes.sh
    ```

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via `kubectl`

## List of Some Files in the Repo

* `app.py` :  The Python flask app to operationalize

* `Dockerfile` : The Docker config file needed to containerize the app

* `Makefile` : A bash script file used to install application dependencies

* `make_prediction.sh` : A script file used to make predictions

* `model_data` : A folder containing housing data information in the Boston area

* `output_txt_files` : A folder containing the result of the prediction

* `requirements.txt` : A text file containing a list of Python app dependencies

* `run_docker.sh` : A script file used to build the Docker image

* `run_kubernetes.sh` : A script file used to build the Kubernetes container

* `upload_docker.sh` : A script file used to push the Docker image to the 
                       remote Docker repository

* `.circleci` :  - A folder that contains CircleCI's config.yml file that 
                   checks the project code for errors

## License

The contents of this repository are covered under the [MIT Licence](#).