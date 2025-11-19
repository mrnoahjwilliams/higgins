# Higgins Homelab Project

## Overview

Higgins is a modular AI assistant system designed to run in a self-hosted homelab environment. It provides a dashboard GUI for monitoring, controlling, and interacting with all components of the homelab. The system is fully containerized using Docker and managed via Docker Compose, allowing for isolated, reproducible, and scalable deployment.

## Features

* **Core AI Assistant:** Higgins runs locally, capable of answering questions about the homelab environment and performing admin-level actions.
* **Dashboard:** Web-based GUI for monitoring and controlling the system, fully interchangeable with Higgins.
* **Containerized Services:** Each module runs in its own Docker container for modularity and isolation.
* **Extensible Modules:** Easily add optional features like algorithm visualizers, additional services, or IoT device integrations.

## Project Structure

```
project-root/
│   docker-compose.yml
│   .dockerignore
│   .gitignore
│   README.md
│
└───core/           # Higgins core code
    │   Dockerfile
    │   requirements.txt
    │   main.py
    │   ...
```

## Prerequisites

* Docker Desktop (Windows/macOS) or Docker Engine (Linux)
* Python 3.11+
* Git (for version control)

## Setup and Installation

1. Clone the repository:

```bash
git clone https://github.com/mrnoahjwilliams/higgins.git
cd higgins
```

2. Build and start the containers:

```bash
docker compose up --build
```

3. Access the dashboard locally:

```
http://localhost:8000
```

4. To stop and clean up containers:

```bash
docker compose down
```

## Development Workflow

* Make changes to your Python code inside `core/`
* Rebuild and restart the container:

```bash
docker compose up --build
```

* View logs in your terminal, test endpoints, and iterate.

## Git Workflow

1. Stage changes:

```bash
git add .
```

2. Commit changes:

```bash
git commit -m "Describe your changes here"
```

3. Push to GitHub:

```bash
git push
```

## Future Enhancements

* Integration with additional homelab hardware.
* Extended API endpoints for remote control and monitoring.
* AI-based automation tasks.
* Modular plugin system for adding optional features.

## License

This project is licensed under the MIT License.

---

*For more information or to contribute, please contact the project maintainer.*
