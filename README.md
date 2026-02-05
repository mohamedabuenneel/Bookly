# Bookly

Bookly is a **RESTful backend service** built with FastAPI, focusing on modular architecture, authentication, and database integration. The project is containerized with Docker for consistent development and production environments.

## Table of Contents

1. [Getting Started](#getting-started)
2. [Prerequisites](#prerequisites)
3. [Project Setup](#project-setup)
4. [Running the Application](#running-the-application)
5. [Running Tests](#running-tests)
6. [Contributing](#contributing)

## Getting Started
Follow the instructions below to set up and run Bookly on your local machine.

### Prerequisites
Make sure you have the following installed:

- Python >= 3.10
- PostgreSQL
- Redis
- Docker (optional, for containerized deployment)

### Project Setup
1. Clone the repository:
    ```bash
    git clone https://github.com/mohamedabuenneel/Bookly.git
    ```
   
2. Navigate to the project directory:
    ```bash
    cd Bookly/
    ```

3. Create and activate a virtual environment:
    ```bash
    python -m venv env
    source env/Scripts/activate   # Windows
    # source env/bin/activate     # Linux/Mac
    ```

4. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

5. Set up environment variables by copying the example configuration:
    ```bash
    copy .env.example .env       # Windows
    # cp .env.example .env       # Linux/Mac
    ```

6. Run database migrations:
    ```bash
    alembic upgrade head
    ```

7. Start the Celery worker (if applicable):
    ```bash
    sh runworker.sh
    ```

## Running the Application
Start the FastAPI server:

```bash
fastapi dev src/
