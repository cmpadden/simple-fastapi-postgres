# Simple FastAPI Postgres Starter

A very basic example of running FastAPI and Postgres with Docker Compose.

## Usage

Build and instantiate the containers:

```sh
docker-compose up -d --build
```

Connect to the Postgres instance running in the `db` container:

```sh
docker-compose exec db psql --username=fastapi_traefik --dbname=fastapi_traefik
```

## References

The scaffolding of this project is a simplified version of fantastic tutorial provided by [testdriven.io](https://testdriven.io/blog/fastapi-docker-traefik/).
