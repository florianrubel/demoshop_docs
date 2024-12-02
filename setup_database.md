# Setup for the databases

## 1. PostgreSQL

Follow this link for detailed instructions: https://www.baeldung.com/ops/postgresql-docker-setup

### 1. Load the image

```bash
docker pull postgres
```

### 2. Run the docker container

!!! Important: Please choose a secure password by yourself.

```bash
docker run -itd -e POSTGRES_USER=demoshop -e POSTGRES_PASSWORD=<password> -p 5432:5432 -v ./data:/var/lib/postgresql/data --name postgresql postgres
```