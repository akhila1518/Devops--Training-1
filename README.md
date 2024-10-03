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
