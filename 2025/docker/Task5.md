# Task 5: Manage Your Image with Docker Hub

## Step 1: Tag Your Image
Before pushing the image, tag it properly:
```sh
docker tag <your-username>/sample-app:latest <your-username>/sample-app:v1.0
```

## Step 2: Push Your Image to Docker Hub
### Log in to Docker Hub (if not already logged in):
```sh
docker login
```

### Push the image:
```sh
docker push <your-username>/sample-app:v1.0
```

## Step 3: Verify by Pulling the Image (Optional)
To confirm that the image was uploaded successfully:
```sh
docker pull <your-username>/sample-app:v1.0
```

This ensures your image is stored in Docker Hub and can be shared or deployed anywhere! 🚀

