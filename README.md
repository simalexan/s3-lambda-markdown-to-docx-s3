
# S3 Bucket -> Lambda (Pandoc Convert Markdown to DOCX) -> S3 Bucket

## Description

This is a serverless component that takes uploaded Markdown files from one S3 Bucket, converts them to Microsoft Word DOCX and uploads to another S3 Bucket. It contains:

- an Input S3 Bucket that accepts files.

- a Lambda that takes the Markdown file from the Input S3 bucket, converts it to a Microsoft Word DOCX and uploads it to the Output one

- an Output S3 Bucket that receives files.

It's a Nuts & Bolts application component for AWS Serverless Application Repository.

## Deployment Parameters

This component has one CloudFormation deployment parameter:

- `ConversionTimeout`, an optional parameter, represents the timeout of the Conversion Lambda function. By default its 60 seconds.

- `InputBucketName`, an optional parameter, represents the name of the Input Markdown Bucket. By default its "s3-lambda-markdown-input-s3-bucket".

- `OutputBucketName`, an optional parameter, represents the name of the Output DOCX Bucket. By default its "s3-lambda-docx-output-s3-bucket".

## Latest Release - 1.1.0

- Added Input and Output bucket names as CloudFormation Parameters

## Roadmap - Upcoming changes

Here are the upcoming changes that I'll add to this serverless component:

- ESLint
- Tests