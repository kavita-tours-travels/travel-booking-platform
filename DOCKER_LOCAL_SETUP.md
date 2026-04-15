# Running Travel Booking Platform Locally with Docker

## Prerequisites

1. **Docker**: Ensure Docker is installed on your machine. You can download it from [Docker's official website](https://www.docker.com/get-started).
2. **Docker Compose**: This is typically included with Docker Desktop, but you can check installation details [here](https://docs.docker.com/compose/install/).

## Steps to Run the Application Locally

### 1. Clone the Repository

First, clone the Travel Booking Platform repository to your local machine:
```bash
git clone https://github.com/<your-username>/travel-booking-platform.git
cd travel-booking-platform
```

### 2. Build the Docker Images

In the project directory, run the following command to build the Docker images:
```bash
docker-compose build
```

### 3. Run the Containers

Next, start the application by running:
```bash
docker-compose up
```
This command will launch the containers as defined in your `docker-compose.yml` file.

### 4. Access the Application

Once the containers are running, you can access the application in your web browser at:
```plaintext
http://localhost:3000
```

### 5. Running Migrations (if applicable)

If your application uses a database and requires migrations, make sure to run:
```bash
docker-compose exec <service_name> npm run migrate
```
Replace `<service_name>` with the service name defined in your `docker-compose.yml`. For example, if your service is named `web`, you would run:
```bash
docker-compose exec web npm run migrate
```

### 6. Stopping the Application

To stop the application, press `CTRL + C` in the terminal where the containers are running. Alternatively, you can run:
```bash
docker-compose down
```

## Troubleshooting

- **Ports already in use**: If you encounter port errors, ensure that the ports defined in your `docker-compose.yml` are not occupied by other applications.
- **Checking logs**: You can view logs for the running containers by executing:
```bash
docker-compose logs
```

## Conclusion

You should now be able to run the Travel Booking Platform locally using Docker. If you encounter any issues, refer to the Docker documentation or consult your project's README for more specific guidance. 

---
*Instructions created on 2026-04-15 22:33:47 (UTC)*