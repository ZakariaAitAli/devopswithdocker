# Use the official golang image as base
FROM golang:1.16

# Set the working directory in the container
WORKDIR /app

# Copy the source code into the container
COPY . .

# Set allowed origin environment variable for CORS
ENV REQUEST_ORIGIN=http://localhost:5000/

# Build the Go binary
RUN go build -o server .

# Expose port 8080
EXPOSE 8080

# Command to run the server
CMD ["./server"]
