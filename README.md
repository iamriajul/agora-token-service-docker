# agora-token-service-docker

[![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/r/iamriajul/agora-token-service)

Docker Hub Tags: https://hub.docker.com/r/iamriajul/agora-token-service/tags

## Example docker-compose.yml

```yaml
version: '3.7'

services:
  agora-token:
    image: iamriajul/agora-token-service:latest # or specify a tag like iamriajul/agora-token-service:1.0.0
    ports:
      - 8080:8080 # the image exposes port 8080
    environment:
      - APP_ID=your-app-id
      - APP_CERTIFICATE=your-app-certificate
      - CORS_ALLOW_ORIGIN=your-allowed-origins
      # Note SERVER_PORT, PORT are not supported, as the image exposes port 8080
      # Passing these env variables will not work
    networks:
      - my-network
```
