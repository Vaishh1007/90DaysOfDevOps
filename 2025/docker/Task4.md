# Task 4: Optimize Your Docker Image with Multi-Stage Builds

## Step 1: Modify Dockerfile for Multi-Stage Build
A multi-stage build helps create a smaller, more efficient Docker image. Here’s how you modify your Dockerfile:

```Dockerfile
# First stage: Build the application
FROM python:3.9-slim AS builder
WORKDIR /app
COPY . /app
RUN pip install -r requirements.txt

# Second stage: Create a lightweight image
FROM python:3.9-alpine
WORKDIR /app
COPY --from=builder /app /app
CMD ["python", "app.py"]
```

## Step 2: Build and Compare Image Sizes
First, build the image:
```sh
docker build -t <your-username>/sample-app:multi-stage .
```
Check the image size before and after using:
```sh
docker images
```
 
## Step 3: Benefits of Multi-Stage Builds
- **Smaller image size** – The final image doesn’t include unnecessary build tools.
- **Faster deployment** – Smaller images load and run quicker.
- **Better security** – Reduces attack surface by removing unused dependencies.

---

