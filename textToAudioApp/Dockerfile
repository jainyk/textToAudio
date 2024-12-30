# Use an official Python runtime as a parent image
FROM python:3.10-slim

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file first to leverage Docker's caching
COPY requirements.txt /app/

# Install dependencies from requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application files into the container
COPY . /app

# Expose the port the Gradio app will run on
EXPOSE 7860

# Command to run the application
CMD ["python", "app.py"]