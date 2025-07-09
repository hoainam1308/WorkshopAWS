---
title : "Create DocumentDB"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

#### Create DocumentDB

1. Open the Amazon DocumentDB console at https://console.aws.amazon.com/docdb

2. In the **Clusters** section, click **Create**

![Create DocumentDB Cluster](/images/3/0034.png?featherlight=false&width=90pc)

3. Select **Instance-based cluster**

4. Under **Number of regular replica instances**, enter the desired number of replicas

![Create DocumentDB Cluster](/images/3/0035.png?featherlight=false&width=90pc)

5. In the **Authentication** section:
   - Enter a username, e.g., `workshopdb`
   - Choose **Self managed**
   - Enter and confirm the **Password**

![Create DocumentDB Cluster](/images/3/0038.png?featherlight=false&width=90pc)

6. Click **Show advanced settings**, and under **Network settings**:
   - Select the **VPC** you created earlier
   - Select the **subnet group** you created  
   {{% notice tip %}}
   If you don't see the VPC listed, try reloading the page.
   {{% /notice %}}

![Create DocumentDB Cluster](/images/3/0037.png?featherlight=false&width=90pc)

7. Scroll back up to the **Connectivity** section and select **Connect to an EC2 compute resource**, then choose the EC2 instance you created.

![Create DocumentDB Cluster](/images/3/0039.png?featherlight=false&width=90pc)

8. (Optional) Uncheck **Enable deletion protection** to make it easier to clean up resources later.

9. Click **Create cluster** to launch the DocumentDB cluster.

![Create DocumentDB Cluster](/images/3/0040.png?featherlight=false&width=90pc)