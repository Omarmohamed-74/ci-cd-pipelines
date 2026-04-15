# Simple Java App - CI/CD Pipeline

## Overview

This project demonstrates a simple Java application integrated with a CI/CD pipeline using GitHub Actions, Docker , Docker Hub, and AWS EKS (Kubernetes).

## Workflow

1. Code is pushed to the `main` branch
2. GitHub Actions workflow is triggered
3. Docker image is built
4. Image is pushed to Docker Hub
5. Application is deployed to Kubernetes (EKS)

## Docker

The application is containerized using Docker and pushed to Docker Hub with the following format:

```
omarmohamed74/app:<branch-name>
```

## Kubernetes

Deployment is managed using Kubernetes manifests:

* Deployment file: `k8s/deployment.yaml`

## Secrets

The following secrets are configured in GitHub:

* `DOCKER_USERNAME`
* `DOCKER_TOKEN`
* `AWS_ACCESS_KEY_ID`
* `AWS_SECRET_ACCESS_KEY`

## How to Run

1. Clone the repository
2. Push changes to the `main` branch
3. The pipeline runs automatically

## Notes

* The EKS cluster must be created beforehand
* The Docker Hub repository must exist
* The Kubernetes cluster must be able to pull the image

## Author

Omar Mohamed

