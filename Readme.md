# Docker Flask Project

### Part 1

## Project Overview

This project demonstrates a simple Flask web application containerized using Docker. The application is built into a Docker image, then pushed to Docker Hub for sharing and deployment. It runs inside a Docker container and displays a basic message on the browser.

---

## Step 1: Build Image

Command:
```bash
docker build -t flask-docker-app .
```

Description:
Builds Docker image from Dockerfile.

Output:
Successfully built image

---

## Step 2: Run Container

Command:
```bash
docker run -d --name flask-container -p 5000:5000 dawoodvision/flask-docker-app
```
Description:
Runs Flask app in container.

Output:
Server started on localhost:5000

---

## Step 3: Docker Login

Command:
```bash
docker login
```

Description:
Login to Docker Hub.

Output:
Login Succeeded

---

## Step 4: Push Image

Command:
```bash
docker push dawoodvision/flask-docker-app
```

Description:
Uploads image to Docker Hub.

Output:
Image uploaded successfully

---

## Docker Hub Repository

https://hub.docker.com/r/dawoodvision/flask-docker-app


### Part 2

# Docker Container Commands

## Project Overview

This project demonstrates the use of different Docker container commands using the Docker image created in Part 1.

Docker Image Used:

dawoodvision/flask-docker-app

---

# Step 1: Run Docker Container

## Command

```bash
docker run -d --name flask-container -p 5000:5000 dawoodvision/flask-docker-app
```
## Command 1: docker ps

```bash
docker ps
```

### Description
Lists all running Docker containers.


### Sample Output
```bash
CONTAINER ID   IMAGE                              STATUS
524eb0aec768   dawoodvision/flask-docker-app     Up 2 minutes
```

## Command 2: docker stop

```bash
docker stop flask-container
```

### Description
Stops a running container.

### Sample Output
```bash
flask-container
```

## Command 3: docker start

```bash
docker start flask-container
```

### Description
Starts a stopped container.
### Sample Output
```bash
flask-container
```

## Command 4: docker rm

```bash
docker rm flask-container
```

### Description
Removes stopped container.
### Sample Output
```bash
flask-container
```

## Command 5: docker logs

```bash
docker logs flask-container
```

### Description
Displays container logs.
### Sample Output
```bash
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:5000
 * Running on http://172.17.0.2:5000
```

## Command 6: docker inspect

```bash
docker inspect flask-container
```

### Description
Displays detailed information about container.
### Sample Output
```bash
JSON formatted container information
```

## Command 7: docker exec

```bash
docker exec -it flask-container bash
```

### Description
Executes bash shell inside running container.
### Sample Output
```bash
root@container:/app#
```

## Command 8: docker commit

```bash
docker commit flask-container flask-new-image
```

### Description
Creates a new image from container.
### Sample Output
```bash
sha256:b4f60519e6af084ed79e23ce93eb2671bedb9ce09db59a7e1cb54e282ef4ce09
```


## Command 9: docker cp

```bash
docker cp flask-container:/app/app.py .
```

### Description
Copies file from container to host machine.

### Sample Output
```bash
File copied successfully
```

## Command 10: docker stats

```bash
docker stats
```

### Description
Displays live resource usage statistics.

### Sample Output
```bash
CPU %, Memory Usage
```
## Command 11: docker top

```bash
docker top flask-container
```

### Description
Displays running processes inside container.

### Sample Output
```bash
python app.py
```

## Command 12: docker pause

```bash
docker pause flask-container
```

### Description
Pauses running container.

### Sample Output
```bash
flask-container
```

## Command 13: docker unpause

```bash
docker unpause flask-container
```

### Description
Unpauses paused container.

### Sample Output
```bash
flask-container
```

## Command 14: docker rename

```bash
docker rename flask-container new-flask-container
```

### Description
Renames a container.

### Sample Output
```bash
Container renamed successfully
```

## Command 15: docker wait

```bash
docker wait new-flask-container
```

### Description
Waits for container to stop and returns exit code.

### Sample Output
```bash
Container renamed successfully
```

## Command 15: docker port

```bash
docker port new-flask-container
```

### Description
Displays mapped ports.

### Sample Output
```bash
5000/tcp -> 0.0.0.0:5000
5000/tcp -> [::]:5000
```

## Command 15: docker update

```bash
docker update --memory 500m --memory-swap 500m new-flask-container
```
### Description
Updates container resource limits.

### Sample Output
```bash
new-flask-container
```
## Command 16: docker restart

```bash
docker restart new-flask-container
```
### Description
Restarts running container.

### Sample Output
```bash
new-flask-container
```

## Command 17: docker wait

```bash
docker wait new-flask-container
```
### Description
Waits for container to stop and returns exit code.

### Sample Output
```bash
Exit code: 137
```