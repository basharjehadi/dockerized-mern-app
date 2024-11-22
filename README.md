# dockerized-mern-app
A simple MERN (MongoDB, Express, React, Node.js) stack three tier application containerized using Docker and Docker compose 
# Create a network for the docker containers
`docker network create demo`

# Build the client
`cd frontend`
`docker build -t frontend .`


# Run the client
`docker run --name=frontend --network=demo -d -p 5173:5173 frontend`
# Verify the client is running
`Open your browser and type http://localhost:5173`
# Run the mongodb container
`docker run --network=demo --name mongodb -d -p 27017:27017 -v ~/opt/data:/data/db mongo:latest`
# Build the server
`cd backend`
`docker build -t backend .`
# Run the server
docker run --name=backend --network=demo -d -p 5050:5050 backend

# Using Docker Compose
`docker compose up -d`

# if everything works you can access the app from browser
![Dashboard](frontend/mern%20app.png)






