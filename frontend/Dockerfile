# Use the official Node.js 16 image as the base image
FROM node:16-alpine

# Set the working directory to /app
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install Expo CLI globally
RUN npm install -g expo-cli

# Install app dependencies
RUN npm install

# Copy the entire project to the working directory
COPY . .

# Build the app
RUN expo build:web

# Expose port 5000 for the app to listen on
EXPOSE 80

# Start the app
CMD ["npm", "start"]
