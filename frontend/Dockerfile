# Base Image
FROM node:latest

# Create app directory
WORKDIR /app

# Install app dependencies
COPY package*.json ./
RUN npm install

# Bundle app source
COPY . .

# Set environment variables
ENV HOST 0.0.0.0
ENV PORT 19006

# Expose the port
EXPOSE 19006

# Start the app
CMD ["npm", "start", "--web"]
