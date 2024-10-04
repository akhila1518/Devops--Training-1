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
    B --> G[utils.py]  %% Added missing closing bracket here
    B --> H[config/]
    H --> I[settings.py]
    B --> J[tests/]
    J --> K[test_main.py]
    J --> L[test_utils.py]

    %% Added a separate subgraph for the second diagram
    subgraph Virtual Machine Setup
        A2[Virtual Machine on AWS] --> B2[EC2 Instance]
        B2 --> C2[Docker Container]
        C2 --> D2[Nginx Web Server]
        B2 -->|Port 80| E2[Open Port on EC2]
        C2 -->|Port 8080| F2[Container Port]

        subgraph Test Process
            G[Test Requests] --> D2
            D2 --> H[Response to Requests]
            H --> G
        end
    end

