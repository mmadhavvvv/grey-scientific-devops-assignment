# Grey Scientific Labs – DevOps Assignment

## About the Assignment
This repository contains my submission for the DevOps assignment shared by Grey Scientific Labs.
The goal of the assignment was to design a basic Docker-based setup along with a CI/CD pipeline,
focusing on configuration and system design rather than actual deployment.

## Project Overview
The system is designed as a simple three-tier application:

User → Nginx → Frontend → Backend → Database

Each part of the system runs in its own container to keep responsibilities clearly separated.
This makes the setup easier to understand, maintain, and scale in the future.

## Docker Setup
Docker Compose is used to define and manage three services:

**Frontend**
- Uses Nginx to serve static frontend content
- Acts as the entry point for user requests

**Backend**
- Represents the application logic layer
- Communicates with the database internally

**Database**
- Uses PostgreSQL
- A Docker volume is used to persist data even if the container restarts

Basic Docker features like volumes, networks, and restart policies are included to resemble a real-world setup.
## Nginx Configuration
Nginx is configured as a reverse proxy:
- Serves frontend content
- Forwards API requests (`/api`) to the backend service

The config is written in a way that allows adding multiple backend instances later for load balancing.

## CI/CD Pipeline
A Jenkins pipeline is defined to show how automation would work in a real environment.
The pipeline includes stages for:
1. Pulling code from GitHub
2. Building Docker images
3. Running tests (placeholder)
4. Deploying containers using Docker Compose

## High Availability and Scalability
Some basic design considerations included in this setup:
- Containers use restart policies for better reliability
- Services communicate over an isolated Docker network
- Nginx can be extended to load balance multiple backend containers
- Database data is stored using persistent volumes
