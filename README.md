# Serverless Image Processing

## 📌 Project Overview

This project demonstrates a **serverless image processing system on AWS**.
Users upload images to an Amazon S3 bucket, and the upload event 
automatically triggers an AWS Lambda function to process the image.

The project uses AWS managed/serverless services, so there is no need to manage servers.

## 🏗️ Architecture

**User → Amazon S3 → AWS Lambda → Processed Image → S3**

### AWS Services Used

* **Amazon S3** – Stores original and processed images
* **AWS Lambda** – Processes images automatically
* **Amazon CloudWatch** – Monitors Lambda execution and logs
* **AWS IAM** – Provides required permissions to Lambda

## ⚙️ How It Works

1. User uploads an image to the S3 bucket.
2. S3 generates an event when the image is uploaded.
3. The event triggers the Lambda function.
4. Lambda processes the image.
5. The processed image is stored in S3.
6. CloudWatch records Lambda logs for monitoring and troubleshooting.

## 🎯 Key Learning

* Understanding serverless architecture
* Working with Amazon S3
* Creating and triggering AWS Lambda functions
* Configuring IAM permissions
* Using CloudWatch for logs and monitoring
* Understanding event-driven architecture

## 🏗️ Architecture Diagram


              ┌──────────────┐
              │     User     │
              └──────┬───────┘
                     │
                     │ Upload Image
                     ▼
              ┌──────────────┐
              │  Amazon S3   │
              │ Input Bucket │
              └──────┬───────┘
                     │
                S3 Event
                     │
                     ▼
              ┌──────────────┐
              │ AWS Lambda   │
              │   Process    │
              │    Image     │
              └──────┬───────┘
                     │
              Processed Image
                     |
              ┌──────────────┐
              │  Amazon S3   │
              │Output Bucket │
              └──────────────┘
                     |
              ┌──────────────┐
              │ CloudWatch   │
              │ Logs/Monitor │
              └──────────────┘
              ┌──────────────┐
              │     IAM      │
              │ Permissions  │
              └──────────────┘

## 📝 Conclusion

This project demonstrates how AWS serverless services can be combined
to build an **automated and scalable image processing workflow without managing traditional servers**.




