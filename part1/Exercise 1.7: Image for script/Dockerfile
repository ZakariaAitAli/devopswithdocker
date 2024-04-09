# Use Ubuntu 22.04 as base image
FROM ubuntu:22.04

# Install curl
RUN apt-get update && apt-get install -y curl

# Copy the script into the container
COPY script.sh /usr/local/bin/script.sh

# Provide execute permissions to the script
RUN chmod +x /usr/local/bin/script.sh

# Set the script to run on container start
CMD ["/usr/local/bin/script.sh"]
