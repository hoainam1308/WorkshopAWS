---
title : "Create VPC"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

#### Create a VPC with Subnets and Related Resources

**ℹ️ Info:** Amazon Virtual Private Cloud (Amazon VPC) allows you to launch AWS resources into a virtual network that you define. This virtual network closely resembles a traditional network in your own data center, with the added benefit of AWS's scalable infrastructure.

Follow the steps below to create a VPC with all the necessary components for deploying your website:

1. Open the Amazon VPC console at https://console.aws.amazon.com/vpc/.

2. On the VPC dashboard, select **Create VPC**.

![Create VPC](/images/2/0001.png?featherlight=false&width=90pc)

3. To create resources, select **VPC and more** to set up a complete VPC environment.

![Create VPC](/images/2/0002.png?featherlight=false&width=90pc)

4. Configure the **Auto-generate** name tag option based on your preference. This allows AWS to automatically create consistent naming for all VPC resources.

5. Enter an IPv4 CIDR block range for your VPC (e.g., 10.0.0.0/16). This defines the IP address range available within your VPC.

6. (Optional) To enable IPv6 support, select **IPv6 CIDR block** and choose an Amazon-provided IPv6 range.

7. For **Number of Availability Zones (AZs)**, select at least two AZs to ensure high availability.

8. Select at least two **private subnets** to create a subnet group for DocumentDB.

9. Review the **Preview** section to see a visual diagram of your configured VPC architecture.

10. Click **Create VPC** to provision all configured resources.

![Create VPC](/images/2/0003.png?featherlight=false&width=90pc)

11. Configure the public subnet:
    - In the VPC console, select the **public subnet**
    - Click **Actions** -> **Edit subnet settings**
    - Check the option **Enable auto-assign public IPv4 address**

![Create VPC](/images/2/0017.png?featherlight=false&width=90pc)