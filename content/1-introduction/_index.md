---
title : "Introduction"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 1. </b> "
---

**Contents:**
- [Project Overview](#project-overview)
- [Amazon DocumentDB](#amazon-documentdb)

#### Project Overview
The e-commerce website project is built with a Node.js backend, MongoDB database, and a React frontend. The system supports essential features such as user registration, login, adding products to the cart, payment, and viewing order history. This serves as a scalable foundation for modern e-commerce applications.

#### Amazon DocumentDB
Amazon DocumentDB is a MongoDB-compatible document database service provided by AWS. It supports two types of clusters (instance-based and elastic) with the ability to scale read/write operations to millions of requests per second. Storage automatically scales up to 128 TiB and supports up to 15 read replicas to improve read performance. It allows flexible compute resource scaling, encrypts data using AWS KMS, operates within a VPC, and supports automated backups with point-in-time recovery. DocumentDB features automatic recovery and failover, while meeting strict security standards such as FedRAMP compliance.

{{< figure src="/images/Arch_Amazon-DocumentDB_16.svg" title="Amazon DocumentDB" width="150pc" >}}