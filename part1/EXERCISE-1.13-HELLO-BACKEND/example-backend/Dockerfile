# Use a golang base image
FROM golang:1.16.15

# Set the working directory in the container
WORKDIR /app

# Copy the source code into the container
COPY . .

# Build the Go binary
RUN go build

# Expose port 8080
EXPOSE 8080

# Command to run the server
CMD ["./server"]