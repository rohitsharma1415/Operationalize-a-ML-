[![RohitS](https://circleci.com/gh/jerrykiz/Operationalize-a-Machine-Learning-Microservice-API.svg?style=svg)](https://circleci.com/gh/jerrykiz/Operationalize-a-Machine-Learning-Microservice-API)

# Operationalize-a-Machine-Learning-Microservice-API

Deploy a containerized Python flask application to serve out predictions (inference) about housing prices through API calls. It uses a a pre-trained, sklearn model that has been trained to predict housing prices in Boston according to several features.

### Install two important components

- Docker
- Virtualbox

I've done it on  Mac with this command:

```
brew cask install virtualbox
```

- For Minikube you have to give this command (on Mac)

```
brew cask install minikube
```

### How the project goes:
minikube start
```
./run_kubernetes.sh
```
./make_prediction.sh
```
minikube delete
``` 

## A short explanation of our files in the repo

- config.yml: CircleCI special file to test the code and get a passed-badge
- app.py: main application, which calculates the predictions
- Dockerfile: Build Docker image
- make_prediction.sh: Send a request to Flask, in order to get the result of a prediction
- Makefile: commands which automatise the environment setup and tests
- run_docker.sh: run Docker
- run_kubernetes.sh: run app in Kubernetes
- upload_docker.sh: upload image to DockerHub
