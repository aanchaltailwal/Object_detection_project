# Object_detection_project

## Yolo5 Object Detection Application - Simplifying Image Analysis with Microservices

## Introduction:

In this project, I've developed a user-friendly object detection service utilizing the powerful Yolo5 deep learning model in 
conjunction with other microservices. The application allows users to easily upload images and promptly receive responses with
detected objects found within the image. Interaction with the application can be accomplished through a simple web user interface (UI) 
or an interactive Telegram bot, offering seamless object detection results to users.

## Architecture:

The application's architecture comprises four key microservices, working together cohesively:

## Unified API Server:

A lightweight Flask UI template facilitates the API server, enabling users to upload images and obtain the detected objects as responses.

## Telegram Bot:

The Telegram bot service plays a crucial role, providing users with a chat-based interface to interact with the object detection service. 
Leveraging the Telegram Bot API, users can submit images and promptly receive detected object results. The Yolo5 service comes into play
to accurately detect objects within the uploaded images. Additionally, both the original and predicted images are uploaded to an AWS S3 
Bucket for further reference.

## Yolo5:

This essential microservice employs a pre-built Yolo5 model, adept at detecting objects in the provided images. It seamlessly detects
multiple objects and uploads both the original and predicted images to an S3 Bucket.

## MongoDB:

The MongoDB service takes care of storing persistent data to ensure smooth functionality.

## Using the Application:

Configuring the microservices to work harmoniously was the main challenge, and this has been successfully achieved through the
docker-compose.yaml file. To initiate the application, run the following command:

- docker-compose up

## Output:
The Yolo5 model excels at detecting multiple objects in the image; however, there might be occasional misclassifications of objects.

## Deployment:

To facilitate the deployment of the application, it has been hosted on both AWS EC2 instances and K8S (Kubernetes). 
The appropriate roles for accessing the S3 bucket have been meticulously configured to ensure a seamless user experience.

Experience the ease of image analysis with our Yolo5 Object Detection Application, as it empowers you with efficient microservices for
rapid and accurate object detection!
