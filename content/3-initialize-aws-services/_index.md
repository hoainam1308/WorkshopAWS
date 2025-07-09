---
title: "Initialize Required AWS Services"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

## EC2

{{< figure src="/images/Arch_Amazon-EC2_64.png" title="Amazon DocumentDB" width="150pc" >}}

Amazon Elastic Compute Cloud (EC2) is a core AWS service that provides scalable computing capacity in the cloud. Below is an overview of EC2: [[1]](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/compute-services.html)

- EC2 allows users to launch virtual servers (called instances) in the AWS cloud environment.
- Supports various instance types optimized for different use cases, offering a mix of CPU, memory, storage, and network capacity.
- Users have full control over EC2 instances, including the ability to start, stop, and terminate them at any time.
- Supports multiple operating systems such as various Linux distributions and Windows Server.
- Offers flexible pricing models: On-Demand, Reserved Instances, and Spot Instances to optimize costs based on workload needs.
- Integrates with other AWS services like Elastic Block Store (EBS) for persistent storage and Auto Scaling for dynamic scaling.
- Security integrations such as VPC, security groups, and key pairs for secure access.
- EC2 instances can be launched across multiple Availability Zones within a region to ensure high availability and fault tolerance.

EC2 is a foundational platform for many cloud-based applications due to its scalability, flexibility, and integration with the AWS ecosystem.

**Source:**  
[[1] AWS Compute Services Overview](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/compute-services.html)

---

## S3

{{< figure src="/images/Arch_Amazon-Simple-Storage-Service_48.png" title="Amazon DocumentDB" width="150pc" >}}

Amazon Simple Storage Service (S3) is a highly scalable, durable, and flexible object storage service provided by AWS. Overview of S3: [[1]](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)

- **Object Storage:** S3 stores data as objects in buckets – ideal for unstructured data like documents, images, and videos. [[2]](https://aws.amazon.com/s3/)
- **Scalability:** Virtually unlimited storage allows businesses to scale as needed.
- **Durability and Availability:** Designed for 99.999999999% (11 9s) durability, ensuring data remains safe.
- **Security:** Supports encryption at rest and in transit, access control policies, and IAM integration.
- **Performance:** Low-latency, high-throughput access makes it suitable for a wide range of applications.
- **Storage Classes:** Multiple tiers such as S3 Standard, Intelligent-Tiering, S3 Glacier help optimize cost based on access patterns.
- **Data Management:** Features like versioning, replication, and lifecycle policies for efficient data lifecycle control.
- **Integration:** Works seamlessly with AWS services like Lambda, CloudFront, Athena, and more.
- **Cost-effective:** Pay-as-you-go pricing based on actual usage.
- **Global Access:** Access your data from anywhere, ideal for global content delivery.

**Sources:**  
[[1] What is Amazon S3?](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)  
[[2] Amazon S3 Overview](https://aws.amazon.com/s3/)

---

## DocumentDB

{{< figure src="/images/Arch_Amazon-DocumentDB_64.png" title="Amazon DocumentDB" width="150pc" >}}

Amazon DocumentDB is a fully managed document database service from AWS, compatible with MongoDB. Overview of DocumentDB: [[1]](https://aws.amazon.com/documentdb/features/)  

- **MongoDB-Compatible:** Supports MongoDB 3.6 and 4.0 APIs – allowing use of existing drivers and tools with minimal changes. [[2]](https://docs.aws.amazon.com/whitepapers/latest/choosing-an-aws-nosql-database/amazon-documentdb.html)  
- **Fully Managed:** AWS handles infrastructure provisioning, patching, backups, and maintenance so developers can focus on building applications. [[3]](https://aws.amazon.com/blogs/publicsector/value-of-document-databases-in-public-sector-amazon-documentdb/)
- **Scalability:** Supports millions of queries per second and auto-scales storage – up to 128 TiB (instance-based) or 4 PiB (Elastic Clusters).
- **High Performance:** Uses distributed, fault-tolerant storage architecture.
- **High Availability:** Data is replicated across multiple Availability Zones.
- **Security:** Network isolation, encryption at rest and in transit, IAM integration for access control.
- **Use Cases:** Ideal for content management systems, user profile stores, mobile backends, and dynamic JSON apps.
- **Data Model:** Stores, queries, and indexes JSON-format data – suitable for flexible schemas.
- **Integration:** Works with AWS Glue, S3, SageMaker, and other services for data processing and machine learning.

**Sources:**  
[[1] Amazon DocumentDB (MongoDB compatible) Features](https://aws.amazon.com/documentdb/features/)  
[[2] Choosing an AWS NoSQL Database – Amazon DocumentDB](https://docs.aws.amazon.com/whitepapers/latest/choosing-an-aws-nosql-database/amazon-documentdb.html)  
[[3] Value of Document Databases in the Public Sector – AWS Blog](https://aws.amazon.com/blogs/publicsector/value-of-document-databases-in-public-sector-amazon-documentdb/)