# Use the latest stable Go version for building the application
FROM golang:1.21 AS builder

# Build arguments
ARG VCS_REF
ARG BUILD_DATE

# Metadata labels
LABEL maintainer="Gautham Prakash <github.com/gauthamp10>"
LABEL org.label-schema.build-date="${BUILD_DATE}"
LABEL org.label-schema.vcs-url="https://github.com/gauthamp10/dockerfile-boilerplates"
LABEL org.label-schema.vcs-ref="${VCS_REF}"

# Set working directory inside the container
WORKDIR /src

# Copy the entire source directory
COPY src /src

# Download dependencies and build the Go binary
RUN go build -o app main.go

# Use a minimal base image for a smaller production build
FROM alpine:latest

# Set working directory
WORKDIR /root/

# Copy the compiled binary from the builder stage
COPY --from=builder /src/app .

# Execution
CMD ["./app"]
