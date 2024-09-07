# Use an official Node.js runtime as the base image
FROM node:20

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install project dependencies
RUN npm ci

# Copy the rest of the application code to the working directory
COPY . .

# Expose a port for the application to listen on
EXPOSE 8080

# Start the application
CMD [ "npm", "run", "prod" ]