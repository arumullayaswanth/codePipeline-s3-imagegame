# AWS S3 + CodePipeline Deployment Guide

This guide deploys the **Images Matching Game** as a static website using S3 and automates updates with CodePipeline.

#### Prerequisites
- AWS account
- GitHub repo with this project

#### Step 1: Create S3 Bucket


#### Step 2: Enable Static Website Hosting


#### Step 3: Add Bucket Policy
Use the policy below (replace `YOUR_BUCKET_NAME`).

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME/*"
    }
  ]
}
```

#### Step 4: Create CodePipeline

#### Step 5: Verify Deployment
1. Open your S3 static website **Endpoint URL**.
2. Confirm the game loads and works.

#### Optional: Versioning
Enable bucket versioning for rollback safety.

#### Cleanup (To Avoid Charges)
- Delete the CodePipeline.
- Delete the S3 bucket.

## Notes
- If you updated HTML/CSS/JS, just push to GitHub. CodePipeline will redeploy automatically.
