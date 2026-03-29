# Проект: Упаковка в Docker Compose

[![Actions Status](https://github.com/raeemu/devops-for-developers-project-74/actions/workflows/hexlet-check.yml/badge.svg)](https://github.com/raeemu/devops-for-developers-project-74/actions)

[![Push to Docker Hub](https://github.com/raeemu/devops-for-developers-project-74/actions/workflows/push.yml/badge.svg?branch=main)](https://github.com/raeemu/devops-for-developers-project-74/actions/workflows/push.yml)

## Requirements

- Docker
- Docker Compose

## Description

This project contains a Dockerized Fastify blog application.

The project uses:
- Docker Compose for local development and tests
- PostgreSQL as a database
- Caddy as a reverse proxy for local HTTPS
- GitHub Actions for CI
- Docker Hub for publishing the production image

Docker Hub image: [raeemu/devops-for-developers-project-74](https://hub.docker.com/repository/docker/raeemu/devops-for-developers-project-74)

## Environment setup

Create a local environment file from the example:

```bash
cp .env.example .env
```

## Available commands

Prepare the project:

```bash
make setup
```

Run tests:

```bash
make test
```

Run local development environment:

```bash
make dev
```

Run CI test command locally:

```bash
make ci
```

Build production image:

```bash
make build
```

Push production image to Docker Hub:

```bash
make push
```

## Local development

Start the application:

```bash
make dev
```

After startup, open:

- `https://localhost`

HTTP requests to `http://localhost` are redirected to HTTPS by Caddy.

## Testing

Run the test environment with Docker Compose:

```bash
make test
```

## Build and publish

Build the production image:

```bash
make build
```

Push the production image to Docker Hub:

```bash
make push
```