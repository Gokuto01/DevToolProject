# Base image
FROM node:14

# Create and set the working directory
WORKDIR /app

# Install Expo globally
RUN npm install -g expo-cli

# Copy package.json and package-lock.json to container
COPY package*.json ./

# Install app dependencies
RUN npm install

# Copy the rest of the app to container
COPY . .

# Set the environment variable for running the app
ENV REACT_NATIVE_PACKAGER_HOSTNAME 0.0.0.0

# Expose the port used by the app
EXPOSE 19006

# Start the app
CMD ["npm", "start", "--", "--web"]
