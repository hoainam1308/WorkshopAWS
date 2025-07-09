---
title : "Deploy Project"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

#### Deployment Steps  
Since the frontend has already been deployed in step [3.3 Create S3 Bucket](3-initialize-aws-services/3-create-s3-bucket), in this section we only need to:

1. [Deploy the backend](4-deploy-project/1-deploy-be-nodejs-ec2)  
2. [Restore data from MongoDB to DocumentDB](4-deploy-project/2-restore-mongo-data-documentdb)  
3. [Test the website](4-deploy-project/3-test-website)