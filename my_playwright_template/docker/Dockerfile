FROM python:3.12-bookworm

WORKDIR /app
ENV PYTHONPATH=/app

COPY .Makefile /app/Makefile
COPY .pyproject.toml /app/pyproject.toml

RUN make venv

RUN mkdir tests
COPY ./tests/ ./tests/

RUN make docker_tests