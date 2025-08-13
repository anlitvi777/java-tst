# Java TST

This project is a simple Java application packaged as a JAR and run with Docker.

## Running with Docker

Use the following steps to start the application along with its PostgreSQL database.

1. **Prerequisites**
   - Install [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://docs.docker.com/compose/install/).

2. **Unzip and Navigate**
   ```bash
   unzip java-tst.zip
   cd java-tst
   ```

3. **Build and Start Containers**
   ```bash
   docker compose up --build
   ```
   If your Docker installation uses the older syntax:
   ```bash
   docker-compose up --build
   ```

4. **Services**
   `docker-compose.yml` defines two services:
   - `db`: PostgreSQL database exposed on port 5432.
   - `app`: Java application exposed on port 8080.

5. **Access the Application**
   - Application: [http://localhost:8080](http://localhost:8080)
   - Database: `localhost:5432` (credentials: `postgres/postgres`, database `demo`).

6. **Stop Containers**
   Press `Ctrl+C` to stop. To remove containers and networks:
   ```bash
   docker compose down
   ```

