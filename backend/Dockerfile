# Use an appropriate base image
FROM python:3.7-slim

# Install system dependencies
RUN apt-get update && apt-get install -y \
    libcrypt1 \
    && rm -rf /var/lib/apt/lists/*

# Set the working directory inside the container
WORKDIR /app

# Copy your application files into the container
COPY . /app

# Install Poetry
RUN pip install poetry

# Install dependencies
RUN poetry config virtualenvs.create false && poetry install --no-dev

# Make port 80 available to the world outside this container
EXPOSE 80

# Command to run your application
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "80"]

