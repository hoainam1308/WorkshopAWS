---
title : "Clean Up Resources"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

## 🧹 Clean Up AWS Resources

After completing your deployment and testing, it's recommended to clean up unused AWS resources to avoid unnecessary charges.

---

### 🪣 Empty S3 Bucket

1. Go to the **Amazon S3 Console**
2. From the bucket list, select the relevant **Bucket**
3. Click **Empty**
4. On the **Empty bucket** page, confirm and click **Empty**

---

### ❌ Delete S3 Bucket

1. Go to **Amazon S3**
2. Select the relevant **Bucket**
3. Click **Delete**, confirm the action, and click **Delete bucket**

---

### 🗑️ Delete DocumentDB Cluster

1. Go to **Amazon DocumentDB**
2. In the **Clusters** list, select the appropriate **Cluster**
3. *(Optional)* If **Deletion protection** is enabled:
   - Click **Actions** → **Modify**
   - Uncheck **Enable deletion protection**
   - Click **Continue** → **Modify cluster**
4. Click **Actions** → **Delete**
5. Confirm and click **Delete**

---

### 💻 Terminate EC2 Instance

1. Exit the SSH session if connected
2. Go to the **Amazon EC2 Console**
3. In the left navigation pane, select **Instances**
4. Select the EC2 instance
5. Click **Instance state** → **Terminate instance**
6. Confirm **Termination**

---

### 🌐 Delete Subnet Group

{{% notice note %}}
You must wait until the DocumentDB cluster is fully deleted before deleting its subnet group.
{{% /notice %}}

1. Go to **Amazon DocumentDB**
2. In the left menu, select **Subnet groups**
3. Select the relevant **Subnet group**
4. Click **Actions** → **Delete**
5. Confirm the **Deletion**

---

### 🔐 Delete Security Groups

1. Go to **Amazon VPC**
2. In the left menu, choose **Security groups**
3. Select all relevant **Security groups**
4. Click **Actions** → **Delete Security groups**
5. Confirm the **Deletion**

---

### 🌐 Delete VPC

1. Go to **Amazon VPC**
2. In the left menu, select **Your VPCs**
3. From the VPC list, select the relevant **VPC**
4. Click **Actions** → **Delete VPC**
5. Confirm the **Deletion**
