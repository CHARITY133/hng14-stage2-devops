# hng14-stage2-devops
Medical Microservices System (DevOps Project)
Overview

This project is a containerized microservices system for handling medical-related tasks. It demonstrates how to build a scalable backend using Docker and background processing.

Architecture

The system includes three main services:

API Service (Python – FastAPI/Flask)
Receives requests and sends tasks to the queue.
Worker Service (Python)
Processes tasks from the queue in the background.
Redis
Acts as a message broker between the API and worker.
Tech Stack
Python
FastAPI / Flask
Redis
Docker
Docker Compose
Project Structure
.
├── api/
├── worker/
├── docker-compose.yml
├── requirements.txt
└── README.md