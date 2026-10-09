# Serverless Image Resizer using AWS

## Project Title and Objective

The Serverless Image Resizer is an AWS-based project that automatically resizes images uploaded to an Amazon S3 bucket.

When a new image is uploaded, an AWS Lambda function is triggered and uses Python with the Pillow library to generate multiple image sizes.

## AWS Services Used

- Amazon S3
- AWS Lambda
- AWS IAM
- Amazon CloudWatch
- Python 3.12
- Pillow (Python Imaging Library)

## Architecture / Workflow

```text
User Uploads Image
        |
        v
   S3 Input Bucket
        |
        v
   S3 Event Trigger
        |
        v
   AWS Lambda Function
        |
        v
   Python + Pillow
        |
        v
   S3 Output Bucket
        |
        v
 Thumbnail | Medium | Large
```

## Implementation Steps

1. Created an Amazon S3 input bucket to store original images.
2. Created a separate S3 output bucket for resized images.
3. Created an AWS Lambda function using Python 3.12.
4. Installed the Pillow library and created a Lambda Layer.
5. Configured IAM permissions for S3 operations.
6. Configured an S3 upload event to trigger Lambda automatically.
7. Processed uploaded images using Python and Pillow.
8. Generated thumbnail, medium, and large image sizes.
9. Stored the processed images in the output bucket.
10. Used Amazon CloudWatch to monitor Lambda executions and troubleshoot errors.

## Image Sizes

- **Thumbnail:** Maximum dimension of 150 pixels.
- **Medium:** Maximum dimension of 500 pixels.
- **Large:** Maximum dimension of 800 pixels.

## Screenshots

Project screenshots will be added here.

## How to Run the Project

1. Create the required S3 input and output buckets.
2. Create the Lambda function using Python 3.12.
3. Add the Pillow dependency through a compatible Lambda Layer.
4. Configure the required IAM permissions.
5. Configure the S3 upload event notification.
6. Upload an image to the input bucket.
7. Verify the resized images in the output bucket.
8. Check CloudWatch logs to verify execution.

## Key Learnings

- Understanding serverless architecture on AWS.
- Configuring S3 event notifications.
- Integrating Amazon S3 with AWS Lambda.
- Processing images using Python and Pillow.
- Creating and attaching Lambda Layers.
- Configuring IAM permissions.
- Monitoring Lambda executions using CloudWatch.
- Troubleshooting access and timeout errors.

## Conclusion

This project demonstrates an automated, event-driven image-processing system using AWS serverless services. It reduces manual image-processing work by automatically generating multiple image sizes whenever an image is uploaded.

## Author

Om Ganesh Parkhi
