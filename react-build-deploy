#!/bin/bash

git clone https://github.com/devops1868/Gold_Site_Ecommerce.git
cd Gold_Site_Ecommerce

image=react

# Build the Docker image
sudo docker build -t ${image} . || true

sudo docker tag ${image} devops1868/${image}

docker push devops1868/${image}:latest

# Continue with other steps
echo "Continuing with the next steps..."

container=reactapp

# Remove the container if it exists
sudo docker rm -f ${container} || true

# Run the container using the correct image and name
sudo docker run -d --name ${container} -p 80:80 ${image} || true
