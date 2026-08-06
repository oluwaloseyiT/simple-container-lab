# Simple Docker Container lab 

This hands-on lab focuses on containerization workflow. I created a Node.js script that prints "Hello, DevOps!", containerizing it with a dockerfile, built the image, and ran the app as a container.

---

## Prerequisite
- A terminal
- Docker installed and running
- Git & Github

---

## Task 1: Prepare your Environment

- Create and open a Local Repo

Create a local project folder to hold your app and Dockerfile.

```
mkdir folder && cd folder
```
---

## Task 2: Setup your App
- Write the app script

Write a simple script (app.js) that the container will run.

```
console.log("Hello, DevOps!");
```
- Write the dockerfile

Define the base image(FROM), copy the app in(COPY), and set the run command(CMD).

```
FROM node:18-alpine
COPY app.js .
CMD ["node", "app.js"]
```
---

## Task 3: Build the App Image

- Build & test the Docker image

Run docker build and then docker run to confirm the container works as expected.
```
docker build -t simple-container-lab .
```
```
docker run --rm simple-container-lab
```
**Note:** Expected output is `Hello, DevOps!`
---

## Task 4: Push to GitHub
- Initialize and then Upload the work to GitHub

---

## License
This project is licensed under the MIT License
