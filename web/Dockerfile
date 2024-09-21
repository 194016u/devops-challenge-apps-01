# Use the latest official Node.js image as the base image
FROM node:latest

# Set the working directory inside the container to /app
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
# This is done first to leverage Docker's cache and avoid reinstalling dependencies
COPY package*.json ./

# Install the app dependencies defined in package.json
RUN npm install

# Copy all other app files from the host to the container's working directory
COPY . .

# Set an environment variable for the port that the app will run on
ENV PORT=3000

# Expose port 3000 to the host (allowing traffic to this port from outside the container)
EXPOSE 3000

# Specify the command to run the app (npm start will run the start script defined in package.json)
CMD ["npm", "start"]

