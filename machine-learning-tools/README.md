# Machine learning Tools
Develop a host of machine learning development and deployment tools and services using reverse image search as a use case.

## Image Similarity dependencies
- Model training
- Model Storage - artifact hub
  - Time server - use to track time for artifact hub 
- Model inference over http - Model Inference container
- Reverse Image search - Approx. Nearest Neighbour Search Engine


## Artifact Hub
A module that helps to manage artefacts in an object store. It tracks the history and versions of an artefact. While it can’t show the difference between different versions it allows actor to push new versions with messages and context around each change and keep track of the time the changes were made.  Artifact Hub web: It may include a web portal to browse through existing artifacts for all clients provided. A store will be required to manage all clients and credentials. Please note that all credentials must be read only for the object store.  Maybe developed in Rust, Go or Python

## Model Inference Container
A container image can pull a model and a script from a url and package it in the container for inference over http. Maybe a different version that can run inference via a message broker or queue. 

## Model Inference Deploy
An http service that can take cluster credentials, script url, model url and generate all the Kubernetes manifests required to deploy the model inference container and also apply those manifests to the specific cluster. It will be a long running api service. Can be built in Rust, Go or python

## Approx. Nearest Neighbour Search Engine
An efficient data store for vectors to find the approximate nearest neighbour efficiently. 

## Time Api
Create an api that returns the current time given a specific timezone
