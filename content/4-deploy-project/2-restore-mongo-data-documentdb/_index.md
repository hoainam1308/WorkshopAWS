---
title : "Restore Data"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

## Steps to Restore Data from MongoDB to DocumentDB

#### Dump Data from Local MongoDB
In this step, we use the [MongoDB Database Tools](https://www.mongodb.com/try/download/database-tools) to export the existing MongoDB data.
1. On your local machine, run the following command:
```bash
mongodump --uri="mongodb://localhost:27017/your_db" --out=dump-folder
```
2. Upload the dump-folder to your EC2 instance under the ec2-user home directory using MobaXterm

#### Restore Data to Amazon DocumentDB
1. Navigate to the EC2 user home directory:
   - Quay về thư mục ec2-user 
   ```bash
   cd ~
   ```
   - Create the MongoDB YUM repository file:
   ```bash
   echo "[mongodb-org-6.0]  
   name=MongoDB Repository  
   baseurl=https://repo.mongodb.org/yum/amazon/2/mongodb-org/6.0/x86_64/  
   gpgcheck=1  
   enabled=1  
   gpgkey=https://pgp.mongodb.com/server-6.0.asc" | sudo tee /etc/yum.repos.d/mongodb-org-6.0.repo
   ```  
   - Install MongoDB tools:
   ```bash
   sudo yum install -y mongodb-org-tools
   ```
2. Restore Data to DocumentDB
   - Download the DocumentDB certificate:
   ```bash
   curl -O https://s3.amazonaws.com/rds-downloads/rds-combined-ca-bundle.pem
   ```
   - Run the mongorestore command (replace the placeholders accordingly):
   ```bash
   mongorestore \
   --host= docdb-xxxxx.cluster-xxxxx.us-east-1.docdb.amazonaws.com \
   --port=27017 \
   --ssl \
   --tlsInsecure \
   --username= YOUR_USER \
   --password= YOUR_PASS \
   --authenticationDatabase=admin \
   dump-folder
   ```

{{% notice warning %}}
To access the restored data from your backend application, make sure the connection URI used in mongoose.connect() includes the database name.
{{% /notice %}}