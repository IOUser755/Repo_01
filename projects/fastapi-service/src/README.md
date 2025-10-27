# FastAPI Service

This directory contains the FastAPI-based microservice. The standard commands for local development and CI are:

| Command | Description |
| ------- | ----------- |
| `uvicorn app.main:app --reload` | Start the development server with auto-reload. |
| `ruff check .` | Run Ruff linting on the codebase. |
| `flake8` | Run Flake8 linting (if configured) for additional style checks. |
| `pytest` | Execute the Python test suite. |

Create a virtual environment and install dependencies listed in `pyproject.toml` or `requirements.txt` before running these commands.
