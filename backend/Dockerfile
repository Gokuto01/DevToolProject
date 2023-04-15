# Use the official Node.js image as the base image
FROM node:14-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Set the environment variable for the port
ENV PORT=3000

# Expose the port on which the application will run
EXPOSE 80

# Start the application
CMD ["npm", "start"]
