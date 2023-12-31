# Start from a base image with Node.js installed
FROM node

# Set the working directory in the container to /app
WORKDIR /app

# Copy the package.json file to the work directory in the container
# This is done before copying the rest of the code to take advantage of Docker's caching mechanism
# If the dependencies in package.json don't change, Docker can use a cached version of the node_modules from a previous build
COPY package.json /app

# Install dependencies in the container
RUN npm install

# Copy the rest of the code to the work directory in the container
COPY . /app

# Expose port 80 to the outside world
EXPOSE 80

# Command to run when the container starts
CMD ["node", "server.js"]