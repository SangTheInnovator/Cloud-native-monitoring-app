# Cloud-native-monitoring-app

## This is a real-time DevOps project using tools like AWS, Docker, Kubernetes, and Python.

### In this Cloud-native DevOps project, we will go through these steps:

1. Create a System Monitoring Application using the Flask framework
2. Run the Python application locally
3. Containerize the application using Docker:
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

- Be using Linux, WSL, or MacOS, with bash, VScode, etc
- [Python 3.8+](https://www.python.org/downloads/) - for running locally, linting, running tests, etc
- [Docker](https://docs.docker.com/get-docker/) - for running as a container, or image build and push
- [Kubectl](https://kubernetes.io/docs/tasks/tools/) - for deploy applications, inspect and manage cluster resources, and view logs
- [AWS CLI](https://aws.amazon.com/cli/) - for deployment to AWS


The application uses the **psutil** and **Flask**, **Plotly**, **boto3**, **kubernetes** libraries. 
Install them using pip command


### Containers

**Dockerfile**

```Dockerfile
# Use the official Python image as the base image
FROM python:3.9-slim-buster

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file to the working directory
COPY requirements.txt .

# Install the required Python packages
RUN pip3 install --no-cache-dir -r requirements.txt 

# Copy the application code to the working directory
COPY . .

# Set the environment variables for the Flask app
ENV FLASK_RUN_HOST=0.0.0.0

# Expose the port on which the Flask app will run
EXPOSE 5000

# Start the Flask app when the container is run
CMD ["flask", "run"]
```

Run in a container with:

```
docker build . -t my-monitoring-app
docker run -p 5000:5000 my-monitoring-app
```

The app runs under Flask and listens on port 5000 by default, this can be changed with the `PORT` environmental variable.


### Kubernetes

- *Create ECR and push the image to the Repo*
   

- *Create EKS cluster and nodes*

- *Create Kubernetes Deployment and Service*


## Screenshot


Clone the project to any directory where you do development work

```
git clone https://github.com/SangTheInnovator/Cloud-native-monitoring-app
```

