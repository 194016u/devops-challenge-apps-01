# Use the latest official Node.js image as the base image
FROM node:latest

# Set the working directory inside the container to /app
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
# This is done first to install dependencies before copying the full app
COPY package*.json ./

# Install the app dependencies defined in package.json
RUN npm install

# Copy all other app files from the host to the container's working directory
COPY . .

# Set an environment variable for the port that the app will run on
ENV PORT=4000

# The default command to run the app (npm start will run the start script defined in package.json)
CMD ["npm", "start"]
