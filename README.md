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

Hit the endpoint using curl / httpie:

```sh
http localhost:8000

HTTP/1.1 200 OK
content-length: 48
content-type: application/json
date: Sun, 17 Sep 2023 19:05:28 GMT
server: uvicorn

[
    {
        "active": true,
        "email": "test@test.com",
        "id": 1
    }
]
```

## References

The scaffolding of this project is a simplified version of fantastic tutorial provided by [testdriven.io](https://testdriven.io/blog/fastapi-docker-traefik/).
