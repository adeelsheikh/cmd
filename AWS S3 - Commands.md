# AWS S3 Commands

## Create S3 bucket

To create a bucket in US East (Ohio) region, following are the minimum required options.

```cmd
aws s3api create-bucket --bucket us-east-1-test-bucket-2019 --region us-east-1
```

To create a bucket in any region other than US East (Ohio), we need to include bucket creation configuration having LocationConstraint option defined same as the region.

```cmd
aws s3api create-bucket --bucket us-east-2-test-bucket-2019 --region us-east-2 --create-bucket-configuration LocationConstraint=us-east-2
```

## Copy files to S3 bucket

```cmd
aws s3 cp D:\TEMP\AdventureWorks.bak s3://contoso-database-backups/staging-dbs
```
