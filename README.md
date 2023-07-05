# Cloud-native-monitoring-app

## This is a real-time DevOps project using tools like AWS, Docker, Kubernetes, and Python.

<br>

### In this Cloud-native DevOps project, we will go through these steps:

1. Create a System Monitoring Application using the Flask framework
2. Run the Python application locally
3. Contanize the application using Docker:
   -  Write Dockerfile
   -  Build a Docker image
   -  Run Docker container
5. Create ECR and push the image to the Repo
6. Create EKS cluster and nodes
7. Create Kubernetes Deployment and Service
8. Post forward and expose the application on Kubernetes
   
<br>

![project_diagram](diagram.png)


## Building & Running Locally

### Pre-reqs

- Be using Linux, WSL or MacOS, with bash, make etc
- [Python 3.8+](https://www.python.org/downloads/) - for running locally, linting, running tests etc
- [Docker](https://docs.docker.com/get-docker/) - for running as a container, or image build and push
- [AWS CLI](https://aws.amazon.com/cli/) - for deployment to AWS

Clone the project to any directory where you do development work

```
git clone https://github.com/SangTheInnovator/Cloud-native-monitoring-app
```

