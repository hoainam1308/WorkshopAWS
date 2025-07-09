---
title : "Create Subnet Group"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

#### Create Subnet Group for DocumentDB

1. Open the Amazon DocumentDB console at https://console.aws.amazon.com/docdb/

2. In the left-hand navigation panel, select **Subnet groups**, then click **Create**.

![Create Subnet Group](/images/2/0014.png?featherlight=false&width=90pc)

3. In the **Subnet group detail** section:
   - Enter a name, e.g., `workshop-documentdb-subnet-group`
   - Enter a description

4. In the **Add subnets** section:
   - Select the **VPC** you created earlier
   - Select **two Availability Zones** that contain subnets
   - For each AZ, select **one private subnet**
   - Click **Add subnet**

![Create Subnet Group](/images/2/0019.png?featherlight=false&width=90pc)

![Create Subnet Group](/images/2/0020.png?featherlight=false&width=90pc)

5. Review the subnet information to ensure accuracy

6. Click **Create** to create the subnet group

![Create Subnet Group](/images/2/0021.png?featherlight=false&width=90pc)

![Create Subnet Group](/images/2/0022.png?featherlight=false&width=90pc)