# Use a node base image
FROM node:16-slim

# Set the working directory in the container
WORKDIR /app

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install dependencies
RUN npm install --production

# Copy the rest of the application files to the container
COPY . .

# Build the static files
RUN npm run build

# Expose port 5000
EXPOSE 5000

# Set environment variable for backend URL
ENV REACT_APP_BACKEND_URL=http://localhost:8080

# Command to run the application
CMD ["npx", "serve", "-s", "-l", "5000", "build"]