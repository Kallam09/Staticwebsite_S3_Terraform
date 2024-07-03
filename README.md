# Terraform AWS S3 Bucket Configuration

This Terraform project automates the setup of an AWS S3 bucket with static website hosting and object uploads.

## Project Overview

This project uses Terraform to create and configure an AWS S3 bucket (`aws_s3_bucket.mybucket`) with the following features:

- **Static Website Hosting**: Configures the S3 bucket to host a static website.
  - `index.html` is set as the index document.
  - `error.html` is set as the error document.

- **Bucket Ownership Controls**: Sets object ownership to "BucketOwnerPreferred" using `aws_s3_bucket_ownership_controls`.

- **Public Access Settings**: Configures public access settings to allow public ACLs and policies with `aws_s3_bucket_public_access_block`.

- **Object Uploads**: Uploads three objects to the bucket:
  - `index.html`: Main HTML file for the website.
  - `error.html`: Custom error page.
  - `profile.png`: Sample image file.

- **Access Control**: Sets bucket ACL to `public-read` for uploaded objects using `aws_s3_bucket_acl`.

## Usage

### Prerequisites

- Install Terraform locally. Download from [Terraform Downloads](https://www.terraform.io/downloads.html).

### Installation and Deployment

1. Clone this repository to your local machine.

2. Navigate to the project directory.

3. Initialize Terraform:
   ```bash
   terraform init
Review and adjust configurations in main.tf and variables.tf as needed.

Apply the Terraform configuration:
