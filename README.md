# [DEPRECATED] PostgreSQL + Adminer with Docker Compose

This repository provides a simple Docker Compose setup for running a PostgreSQL database alongside [Adminer](https://www.adminer.org/) — a lightweight database management tool.

## 📦 Services

- **DB**

  - Official image: `postgres`
  - Default Username: `postgres`
  - Default Password: `postgres`
  - Default database: same as username

- **Adminer**
  - Official image: `adminer`
  - Web UI for interacting with PostgreSQL via browser

## 🛠 Prerequisites

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## 🚀 Quick Start

1. Create a .env file (optional but recommended):

```bash
POSTGRES_USER=test
POSTGRES_PASSWORD=admin123
POSTGRES_DB=test_db
```

2. Start the services:

```bash
docker-compose up -d
```

3. Open Adminer in your browser:

```shell
http://localhost:8080
```

4. Use the following credentials to connect:

- System: PostgreSQL
- Server: db
- Username: [Your Username]
- Password: [Your Password]
- Database: [Your Database]

## Shutdown

To stop and remove containers:

```bash
docker-compose down
```

To also remove volumes (erases all data):

```bash
docker-compose down -v
```

## File Structure

```
├── .env (optional)
├── .gitignore
├── docker-compose.yml
└── README.md
```
