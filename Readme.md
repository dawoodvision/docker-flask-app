# Docker Flask Project

## Project Overview

This project demonstrates a simple Flask web application containerized using Docker. The application is built into a Docker image, then pushed to Docker Hub for sharing and deployment. It runs inside a Docker container and displays a basic message on the browser.

---

## Step 1: Build Image

Command:
docker build -t flask-docker-app .

Description:
Builds Docker image from Dockerfile.

Output:
Successfully built image

---

## Step 2: Run Container

Command:
docker run -p 5000:5000 flask-docker-app

Description:
Runs Flask app in container.

Output:
Server started on localhost:5000

---

## Step 3: Docker Login

Command:
docker login

Description:
Login to Docker Hub.

Output:
Login Succeeded

---

## Step 4: Push Image

Command:
docker push dawoodvision/flask-docker-app

Description:
Uploads image to Docker Hub.

Output:
Image uploaded successfully

---

## Docker Hub Repository

https://hub.docker.com/r/dawoodvision/flask-docker-app