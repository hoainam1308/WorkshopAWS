---
title : "Create Security Group"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

#### Create Security Group for EC2

**ℹ️ Info:** Security groups act as virtual firewalls for Amazon EC2 instances, controlling inbound and outbound traffic.  
For the DocumentDB deployment, we need to create a security group for the EC2 instances that will connect to our database.

Follow these steps to create a Security Group with the necessary ports:

1. Open the Amazon VPC console at https://console.aws.amazon.com/vpc/.

2. In the VPC navigation panel, under **Security**, choose **Security groups**.

3. Click **Create security group**.

![Create Security Group](/images/2/0004.png?featherlight=false&width=90pc)

4. In the **Basic details** section:  
   - Enter a name for the security group, e.g., `workshop-ec2-sg`  
   - Add a description  
   - For **VPC**, select the one created previously

5. In the **Inbound rules** section, click **Add rule** and configure access:
   - Type: **SSH**, Source: **My IP**
   - Type: **HTTP**, Source: **Anywhere**
   - Type: **HTTPS**, Source: **Anywhere**
   - Type: **Custom TCP**, Port range: **3000**, Source: **Anywhere**

   {{% notice note %}}
   For production environments, restrict SSH access to trusted IP ranges instead of allowing access from anywhere (0.0.0.0/0).
   {{% /notice %}}

![Create Security Group](/images/2/0005.png?featherlight=false&width=90pc)

6. Review your settings and click **Create security group**.

![Create Security Group](/images/2/0006.png?featherlight=false&width=90pc)

7. After creation, the new security group will appear in the list. Take note of its ID as you will need it when launching an EC2 instance.

![Create Security Group](/images/2/0007.png?featherlight=false&width=90pc)


#### Create Security Group for DocumentDB

Follow these steps to create a Security Group for DocumentDB with the required port:

1. From the **Security Groups** list, click **Create security group**.  
![Create Security Group](/images/2/0008.png?featherlight=false&width=90pc)

2. In the **Basic details** section:  
   - Enter a name for the se