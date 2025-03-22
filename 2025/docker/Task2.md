# Task 2: Create a Dockerfile for a Sample Project

## Step 1: Choose a Simple Application
Pick a basic app, such as:
- A Python program that prints "Hello, Docker!"
- A simple Node.js or Java app that serves a web page

## Step 2: Create a Dockerfile
A `Dockerfile` tells Docker how to build and run your app. Below is an example for a **Python app**:

```Dockerfile
# Base Python image
FROM python:3.9-slim

# Set working directory inside container
WORKDIR /app

# Copy all files from your computer to container
COPY . .

# Install dependencies from requirements.txt
RUN pip install -r requirements.txt

# Running on port 
EXPOSE 80

# Command to start the application
CMD ["python", "app.py"]
```

### **Explanation of the Dockerfile:**
- `FROM python:3.9-slim` → Uses a small Python version to save space.
- `WORKDIR /app` → Sets `/app` as the working folder inside the container.
- `COPY . .` → Copies your all files into the container.
- `RUN pip install -r requirements.txt` → Installs necessary Python packages.
- `EXPOSE 80` → Running on port 80
- `CMD ["python", "app.py"]` → Runs `app.py` when the container starts.

## Step 3: Build Your Docker Image
Run this command in your terminal to create a Docker image:
```sh
docker build -t <your-username>/sample-app:latest .
```

## Step 4: Run and Test Your Container
Run your app inside a container:
```sh
docker run -d -p 8080:80 <your-username>/sample-app:latest
```

### Check if the container is running:
```sh
docker ps
```

### View logs to confirm it works:
```sh
docker logs <container_id>
```

If everything is set up correctly, your app should be running inside a Docker container! 🚀

