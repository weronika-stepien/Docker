# Base image with Python
FROM python:3.9-slim

# Switch to root user to install tools
USER root

# Install necessary tools and dependencies for the CI/CD process
RUN apt-get update && \
    apt-get install -y \
    git \
    docker.io \
    curl \
    jq \
    wget \
    unzip && \
    apt-get clean


# Install Python dependencies (pipenv or pip)
RUN pip install --no-cache-dir pipenv

# Ensure Docker can be accessed by Jenkins user (if a user exists)
RUN groupadd -g 1000 jenkins && \
    useradd -m -u 1000 -g jenkins jenkins && \
    usermod -aG docker jenkins

# Switch back to the Jenkins user
USER jenkins

# Set the default working directory
WORKDIR /workspace

