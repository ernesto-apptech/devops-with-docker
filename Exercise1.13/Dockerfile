# We need JAVA 8
FROM golang:1.16.15

# Creates an app directory to hold your app’s source code
WORKDIR /app
 
# Copies everything from your root directory into /app
COPY . .
 
# Installs Go dependencies
RUN go mod download
 
# Builds your app with optional configuration
# RUN go build -o /godocker

# ENV PATH=$PATH:/usr/local/go/bin
# ENV REQUEST_ORIGIN=http://localhost 
# Build
RUN go build

# Tells Docker which network port your container listens on
EXPOSE 8080

# Run
CMD ["./server"]