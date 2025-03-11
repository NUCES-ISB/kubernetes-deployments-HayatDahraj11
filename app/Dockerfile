# Use the official Python image from Docker Hub
FROM python:3.9-slim

# Install PostgreSQL development dependencies
RUN apt-get update && apt-get install -y libpq-dev gcc

# Set the working directory in the container
WORKDIR /app

# Copy the requirements.txt to the container
COPY requirements.txt .

# Install the dependencies
RUN pip install -r requirements.txt

# Copy the rest of the application files to the container
COPY . .

# Expose the port the app will run on
EXPOSE 5000

# Set the default command to run the Flask app
CMD ["python", "app.py"]
