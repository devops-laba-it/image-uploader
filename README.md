# Image-Uploader

This is an application designed to retrieve images from an SQS queue, process them, and store them in S3.

## Lambda Function

For deployment on AWS, a Lambda function has been utilized. It is triggered by the appearance of a message in the SQS queue.

## Environment Variables

The application relies on environment variables, which need to be configured in AWS.

- `BOOKS_AWS_ACCESS_KEY_ID`
- `BOOKS_AWS_SECRET_ACCESS_KEY`
- `BOOKS_AWS_REGION`
- `BUCKET_NAME`

## Pipeline

```bash
make lint
```

To generate the `app.zip` file, execute the following command:

```bash
make build
```

The resulting file should be uploaded to AWS as a Lambda function.