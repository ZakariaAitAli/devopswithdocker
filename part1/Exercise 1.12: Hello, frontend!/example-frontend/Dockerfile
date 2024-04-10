# Use Node LTS version as base image
FROM node:16-slim

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Build the static files
RUN npm run build

# Install serve globally
RUN npm install -g serve

# Expose port 5000
EXPOSE 5000

# Command to serve the project
CMD ["serve", "-s", "-l", "5000", "build"]
