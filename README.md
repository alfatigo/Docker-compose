# KinetEco Compose – Multi-Service Docker Environment

## Project Description

KinetEco Compose is a practical environment designed to deploy a multi-service application using Docker Compose. The project includes a web storefront, a backend scheduler service, and a MySQL database. All components are containerized and configured for local development and testing.

## Project Structure
  ```
  KinetEco-Compose/
  ├── mysql/
  │   ├── db.sql
  │   ├── env.vars
  │   └── env_vars
  │
  ├── scheduler/
  │   ├── Dockerfile
  │   ├── index.html
  │   └── JS, CSS, and image files
  │
  ├── storefront/
  │   ├── Dockerfile
  │   ├── index.html
  │   └── product images, styles, and scripts
  │
  ├── docker-compose.yaml
  ├── LICENSE
  └── README.md

  ```

## Services

### storefront (Frontend)
- Contains the public-facing web interface of KinetEco.
- Exposed at http://localhost:7575 and https://localhost:1443.
- Built from the `storefront/` Dockerfile.

### scheduler (Backend)
- Represents a backend or scheduling process.
- Exposed at http://localhost:8989.
- Built from the `scheduler/` directory.

### database (MySQL)
- Uses the official `mysql:latest` image.
- Loads environment variables from `mysql/env_vars`.
- Uses a named volume `kineteco` for data persistence.
- Executes any initialization scripts found in the `mysql/` directory.

## How to Run

### 1. Requirements

- Docker: https://docs.docker.com/get-docker/
- Docker Compose: https://docs.docker.com/compose/

### 2. Clone the Repository

```bash
git clone https://github.com/yourusername/KinetEco-Compose.git
cd KinetEco-Compose
