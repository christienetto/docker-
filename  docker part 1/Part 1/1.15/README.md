# Frontend Docker Setup for mpvssh

This directory contains the necessary configuration to build and run the frontend part of the **mpvssh** project inside a Docker container.

## Prerequisites

Before running the frontend in a Docker container, make sure you have the following:

- Docker installed on your machine. If you don’t have it yet, follow the [official Docker installation guide](https://docs.docker.com/get-docker/).
- Node.js (as the frontend is built using React/Expo).

## Dockerfile Overview

The Dockerfile in this directory sets up an environment for building and running the frontend of the **mpvssh** project. It uses a Node.js image, installs the necessary dependencies, builds the project, and serves it on port `5000`.

### Steps in the Dockerfile:

1. **Base Image**: Uses the official `node:16-alpine` image, which provides a lightweight Node.js environment based on Alpine Linux.
2. **Working Directory**: Sets the working directory inside the container to `/app`.
3. **Dependencies Installation**: Copies `package.json` and `package-lock.json` (or `yarn.lock`) into the container and installs the frontend dependencies with `npm install`.
4. **Build the Frontend**: Builds the frontend React/Expo project using `npm run build`.
5. **Serving the Application**: Installs the `serve` package globally to serve the built files and exposes the app on port `5000`.

## Building and Running the Frontend

To build and run the frontend Docker container, follow these steps:

1. **Navigate to the frontend directory**:

   ```bash
   cd /path/to/mpvssh/frontend


   
