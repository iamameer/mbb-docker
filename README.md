
# mbb-docker

MBB Docker is the docker-compose setup for:
- [mbb-fe](https://github.com/iamameer/mbb-fe) (Frontend)
- [mbb-be](https://github.com/iamameer/mbb-be) (Backend)

## 1. Pre-requisites

Ensure Docker is installed on your system. Follow the installation guide for your operating system:
- [Install Docker](https://docs.docker.com/desktop/setup/install/)

## 2. Steps to Run

### 2.1. Setup the Project Structure

Place the `docker-compose.yml` file in the root directory where both the `/mbb-fe` and `/mbb-be` directories are located.

```
project-root/
├── docker-compose.yml
├── mbb-fe/
│   └── (frontend code)
└── mbb-be/
    └── (backend code)
```

### 2.2. Pull the Latest Versions

Ensure you have the latest updates for both repositories:
```bash
git pull origin main
```

### 2.3. Build and Start the Containers

Run the following command to build and start the containers:
```bash
docker-compose up -d --build
```

This will build the images and run the services in detached mode.

## 3. Check Running Services

- **API**: Visit [http://localhost:3000](http://localhost:3000) to test if the backend API is running.
- **Frontend**: Visit [http://localhost:5173](http://localhost:5173) to test if the frontend is running.

## 4. View Logs

To monitor logs for all services, open another terminal and run:
```bash
docker-compose logs -f
```

## 5. Check Status

To check the status of the running services, run:
```bash
docker-compose ps
```

## 6. Restart the Services

To restart the services:
```bash
docker-compose down
docker-compose up
```
