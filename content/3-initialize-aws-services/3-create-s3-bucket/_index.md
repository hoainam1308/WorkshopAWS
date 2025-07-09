---
title : "Create S3 Bucket"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---

#### Create S3 Bucket

1. Open the Amazon S3 Console at https://console.aws.amazon.com/s3 and click **Create bucket**.

![Create S3 Bucket](/images/3/0052.png?featherlight=false&width=90pc)

2. Enter a bucket name, for example: `workshop-s3-fe`.

![Create S3 Bucket](/images/3/0053.png?featherlight=false&width=90pc)

3. Uncheck **Block all public access** and check the acknowledgment box below.

![Create S3 Bucket](/images/3/0054.png?featherlight=false&width=90pc)

4. Review the settings and click **Create bucket**.

![Create S3 Bucket](/images/3/0055.png?featherlight=false&width=90pc)

![Create S3 Bucket](/images/3/0056.png?featherlight=false&width=90pc)

5. In the **Permissions** tab of the newly created bucket, go to **Bucket policy**, click **Edit**, and paste the following code into the **Policy** field:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::workshop-s3-fe/*"
    }
  ]
}
```

![Create S3 Bucket](/images/3/0058.png?featherlight=false&width=90pc)

![Create S3 Bucket](/images/3/0060.png?featherlight=false&width=90pc)

![Create S3 Bucket](/images/3/0061.png?featherlight=false&width=90pc)

6. Click **Save changes**

![Create S3 Bucket](/images/3/0062.png?featherlight=false&width=90pc)

![Create S3 Bucket](/images/3/0063.png?featherlight=false&width=90pc)

7. Retrieve the EC2 public IP address to configure the VITE_BACKEND_URL for the React frontend.

8. Build Frontend:
   - Open the React frontend project in Visual Studio Code
   - Update the environment variable ```VITE_BACKEND_URL``` in the .env file
   - Run the build command: ```npm run build```. This will generate a **dist** or **build** folder

![Create S3 Bucket](/images/3/0059.png?featherlight=false&width=90pc)

9. Upload the contents of the build folder to the S3 bucket:
   - In the **Objects** tab of the S3 bucket, click **Upload**
   ![Create S3 Bucket](/images/3/0064.png?featherlight=false&width=90pc)
   - Drag and drop all files/folders from the build directory into the **Upload** area
   ![Create S3 Bucket](/images/3/0065.png?featherlight=false&width=90pc)
   ![Create S3 Bucket](/images/3/0066.png?featherlight=false&width=90pc)
   - Click **Upload** and wait for the upload to complete
   ![Create S3 Bucket](/images/3/0069.png?featherlight=false&width=90pc)
   ![Create S3 Bucket](/images/3/0070.png?featherlight=false&width=90pc)


10. Enable static website hosting
   - Go to the **Properties** tab of the bucket, scroll to **Static website hosting**, and click **Edit**
   ![Create S3 Bucket](/images/3/0071.png?featherlight=false&width=90pc)
   ![Create S3 Bucket](/images/3/0072.png?featherlight=false&width=90pc)
   - Check **Enable** for **Static website hosting**
   - In the **Index document** field, enter ```index.html```
   ![Create S3 Bucket](/images/3/0073.png?featherlight=false&width=90pc)
   - Click **Save changes**, then test the frontend site
   ![Create S3 Bucket](/images/3/0074.png?featherlight=false&width=90pc)
   ![Create S3 Bucket](/images/3/0075.png?featherlight=false&width=90pc)