---
title: "Week 4 Worklog"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Understand and use S3 for object storage and static website hosting.
* Deploy RDS to manage relational databases on AWS.
* Get familiar with DynamoDB — AWS's serverless NoSQL database.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Review EC2 and Auto Scaling knowledge from last week <br> - Read S3 documentation: storage classes, versioning, lifecycle <br> - Study differences between SQL and NoSQL | 05/11/2026 | 05/11/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Tue | **Lab 7: Static Website Hosting with Amazon S3** <br> - Create an S3 bucket and configure access permissions <br> - Enable versioning and lifecycle policy <br> - Host a static website on S3 <br> - Configure bucket policy and CORS <br> - Use AWS CLI to upload/download objects | 05/12/2026 | 05/12/2026 | <https://000057.awsstudygroup.com/> |
| Wed | **Lab 8: Database Essentials with Amazon RDS** <br> - Study RDS: supported engines, Multi-AZ, Read Replica <br> - Create an RDS MySQL instance in a private subnet <br> - Connect to RDS from EC2 <br> - Create a Read Replica and perform a failover <br> - Configure automated backups and snapshots | 05/13/2026 | 05/13/2026 | <https://000005.awsstudygroup.com/> |
| Thu | **Lab 9: NoSQL Database Essentials with Amazon DynamoDB** <br> - Study DynamoDB: partition key, sort key, GSI, LSI <br> - Create a DynamoDB table and perform CRUD operations <br> - Learn DynamoDB capacity modes (On-demand vs Provisioned) <br> - Enable DynamoDB Streams <br> - Explore DAX (DynamoDB Accelerator) | 05/14/2026 | 05/15/2026 | <https://000060.awsstudygroup.com/> |
| Fri | - Review and consolidate Week 4 knowledge <br> - Compare when to use RDS vs DynamoDB <br> - Design a data model for a sample application | 05/15/2026 | 05/15/2026 | |

### Week 4 Achievements:

* Used Amazon S3 proficiently:
  * Managed bucket permissions, object access, and bucket policies
  * Configured versioning to protect data from accidental deletion
  * Set up lifecycle rules to optimize storage costs
  * Deployed a static website on S3

* Deployed and managed RDS:
  * Created an RDS instance in a private subnet with correct security groups
  * Configured Multi-AZ for high availability
  * Created a Read Replica to scale read operations
  * Practiced backup and restore from snapshots

* Worked with DynamoDB:
  * Designed a data model with proper partition key and sort key
  * Performed efficient query and scan operations
  * Understood the difference between On-demand and Provisioned capacity
  * Configured DynamoDB Streams for event-driven processing
