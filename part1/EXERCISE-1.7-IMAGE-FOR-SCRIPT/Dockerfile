# Start from Ubuntu 22.04
FROM ubuntu:22.04

# Install curl
RUN apt update && apt install -y curl

# Copy the script file into the image
COPY script.sh /usr/src/app/script.sh

# Set the script to run on container start using CMD
CMD ["sh", "/usr/src/app/script.sh"]
