---
title : "Create EC2 Instance"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---

**ℹ️ Info:** Amazon EC2 (Elastic Compute Cloud) provides scalable computing capacity in the AWS Cloud, eliminating the need for upfront hardware investment.

To create a Linux EC2 instance using the AWS Management Console, follow the steps below. This guide will help you quickly launch your first instance with the required configuration.

#### Create EC2 Instance

1. Open your web browser and navigate to the Amazon EC2 Console at https://console.aws.amazon.com/ec2/.

![Create EC2](/images/3/0024.png?featherlight=false&width=90pc)

2. In the left navigation pane, under **Instances**, select **Instances**, then click **Launch instances**.

3. Enter a name, e.g., `workshop-ec2`.

4. Under **Application and OS Images**:
   - Choose **Amazon Linux**
   - Under **Amazon Machine Image (AMI)**, select **Amazon Linux 2 AMI**

![Create EC2](/images/3/0025.png?featherlight=false&width=90pc)

5. Select **t2.micro** under **Instance type**

![Create EC2](/images/3/0026.png?featherlight=false&width=90pc)

6. Under **Key pair**, select **Create new key pair**:
   - Enter a name for the key pair, e.g., `my-workshop-keypair`
   - For **Key pair type**, choose **.RSA**
   - For **Private key file format**, choose **.pem**
   - Click **Create key pair** and save the file securely

![Create EC2](/images/3/0027.png?featherlight=false&width=90pc)

7. Under **Network settings**, click **Edit**:
   - Select the **VPC** you created earlier
   - Choose a **public subnet** that has **Auto-assign public IP** enabled
   - Select **Use existing security group**
   - Choose the security group you created for EC2: `workshop-ec2-sg`

![Create EC2](/images/3/0028.png?featherlight=false&width=90pc)

![Create EC2](/images/3/0029.png?featherlight=false&width=90pc)

8. Review the **Summary** and click **Launch instance**

![Create EC2](/images/3/0031.png?featherlight=false&width=90pc)

![Create EC2](/images/3/0022.png?featherlight=false&width=90pc)