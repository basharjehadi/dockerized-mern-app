# dockerized-mern-app

# Create a network for the docker containers

# Build the client
`cd frontend`
`docker build -t frontend .`


# Run the client
`docker run --name=frontend --network=mern -d -p 5173:5173 frontend`
# Verify the client is running
`Open your browser and type http://localhost:5173`
# Run the mongodb container
`docker run --network=mern --name mongodb -d -p 27017:27017 -v ~/opt/data:/data/db mongo:latest`
# Build the server
`cd backend`
`docker build -t backend .`
# Run the server
docker run --name=backend --network=demo -d -p 5050:5050 mern-backend

# Using Docker Compose
`docker compose up -d`





