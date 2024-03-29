# Use the official Go image with version 1.18 as the base image
FROM golang:1.18

# Set the working directory inside the container
WORKDIR /app

# Copy the go.mod and go.sum files to the working directory
COPY go.mod go.sum ./

# Download and cache dependencies
RUN go mod download

# Copy the rest of the application source code
COPY . ./

# Compile the Go application
RUN go build -o /go-server

# Expose port 8080 to the outside world
EXPOSE 8080

# Command to run the executable
CMD ["/go-server"]

