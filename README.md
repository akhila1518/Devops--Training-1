# Project Title

## Project Overview

This project is designed to run a Docker container that encapsulates the application. Below is the structure of the project.

## Project Structure

## Docker Architecture with Nginx

```mermaid
graph TD;
    A[Virtual Machine on AWS] --> B[EC2 Instance]
    B --> C[Docker Container]
    C --> D[Nginx Web Server]
    B -->|Port 80| E[Open Port on EC2]
    C -->|Port 8080| F[Container Port]

    G[Test Requests] --> D
    D --> H[Response to Requests]
    H --> G

