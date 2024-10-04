# Project Title

## Project Overview

This project is designed to run a Docker container that encapsulates the application. Below is the structure of the project.

## Project Structure

```mermaid
graph TD;
    A[Dockerfile] -->|builds| B[app]
    A --> C[requirements.txt]
    A --> D[.dockerignore]
    A --> E[README.md]
    B --> F[main.py]
    B --> G[utils.py]

    B --> H[config/]
    H --> I[settings.py]
    B --> J[tests/]
    J --> K[test_main.py]
    J --> L[test_utils.py]

graph TD;
    A[Virtual Machine on AWS] --> B[EC2 Instance]
    B --> C[Docker Container]
    C --> D[Nginx Web Server]
    B -->|Port 80| E[Open Port on EC2]
    C -->|Port 8080| F[Container Port]

    subgraph Test Process
        G[Test Requests] --> D
        D --> H[Response to Requests]
        H --> G
    end

