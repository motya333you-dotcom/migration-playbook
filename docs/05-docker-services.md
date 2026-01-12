# 05 - Docker Services

## Purpose

This chapter describes **setting up application services in Docker** for the migrated environment.

Scope 1.0: keep it simple, reproducible, and documented.

---

## Step 1 - Prepare Docker Compose

- Create `docker-compose.yml` for each service
- Include:
  - service image
  - environment variables
  - volume mounts
  - network configuration

Example:

```yaml
version: "3.9"
services:
  web:
    image: nginx:latest
    ports:
      - "80:80"
    volumes:
      - ./html:/usr/share/nginx/html
  app:
    image: myapp:latest
    environment:
      - ENV=production
    depends_on:
      - db
  db:
    image: postgres:14
    volumes:
      - db_data:/var/lib/postgresql/data
volumes:
  db_data:
## Step 2 - Run Containers

Test docker-compose up -d for each service
Ensure containers start without errors
Check logs using docker-compose logs -f

## Step 3 - Data Persistence
Mount volumes for persistent data
Ensure data survives container restarts
Test snapshot + restore cycle to verify integrity

## Step 4 - Networking Between Services
Use Docker networks for service communication
Verify app ↔ database connectivity
Document IPs, ports, and network rules

## Step 5 - Verification & Testing
Restart all containers and confirm services run correctly
Check logs for errors
Test end-to-end functionality of migrated services
