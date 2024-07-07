
FROM python:3.7-slim

# Install system dependencies
RUN apt-get update && apt-get install -y \
    libcrypt1 \
    && rm -rf /var/lib/apt/lists/*

# Set the working directory inside the container
WORKDIR /app

# Copy your application files into the container
COPY . /app

# Install necessary Python packages
RUN pip install -r requirements.txt

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable if needed
ENV NAME World

# Command to run your application
CMD ["python", "app.py"]

