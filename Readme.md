# Dockerized Node.js App

## About

This project is a **Node.js application containerized with Docker**. It runs a server on **port 3000** and demonstrates how to package a Node.js app for consistent deployment across different environments.

> **Note on language/runtime:** Although GitHub detects this repository as **JavaScript** (based on the `.mjs`/`.js` files), the project runs on the **Node.js runtime**, not Java. Node.js executes JavaScript code on the server-side using the V8 engine.

---

## Features

- Runs a **Node.js server** inside a Docker container  
- Exposes **port 3000** for browser access  
- Uses a **Dockerfile** for building the container image  
- Automatically installs dependencies using **npm**  
- Suitable for learning **Node.js + Docker basics**  

---

## Prerequisites

- [Docker](https://www.docker.com/get-started) installed and running  
- Internet connection (for pulling the Node.js base image and npm dependencies)  
- Optional: Firewall exceptions to allow port 3000 access  

---

## Getting Started

### 1. Clone the repository
```bash
git clone <your-repo-url>
cd <repo-folder>

2. Build the Docker image

docker build -t my-node-app .

3. Run the Docker container

docker run -p 3000:3000 my-node-app

Open your browser at http://localhost:3000 to see the app running.

4. Running in detached mode (optional)

docker run -d -p 3000:3000 --name my-node-app my-node-app
docker logs -f my-node-app   # to follow logs

Folder Structure

first-demo-starting-setup/
│   Dockerfile
│   package.json
│   app.mjs
│   README.md
Dockerfile – Instructions to build the container image

package.json – Node.js dependencies and scripts

app.mjs – Main application entry point (Node.js server)

Troubleshooting
If the server is not accessible in the browser, check Windows Firewall notifications and allow Docker to expose port 3000.

To see logs of a running container:

docker logs <container-id-or-name>
To stop the container:

docker stop my-node-app
Notes
This repository is intended for learning purposes and demonstrates Dockerized Node.js app deployment.

Modify app.mjs to experiment with different Node.js functionality or endpoints.
