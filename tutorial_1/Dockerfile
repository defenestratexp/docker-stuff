# Select an image
FROM python:2.7-slim

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container in the working directory /app
COPY . /app

# Install any needed packages
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Open a port from the container to the world
EXPOSE 80

# Environment variables
ENV NAME World

# Run app.py when the container launches
cmd ["python", "app.py"]
