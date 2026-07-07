---
title: "Week 7 Worklog"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Build a serverless backend with AWS Lambda and API Gateway.
* Use AWS Systems Manager to manage and operate an EC2 fleet.
* Implement AWS Backup for comprehensive data protection.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Review CI/CD and Container knowledge from last week <br> - Read documentation on Serverless architecture <br> - Study event-driven architecture patterns | 06/01/2026 | 06/01/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Tue | **Lab 16: Serverless Automation with AWS Lambda** <br> - Study Lambda: triggers, execution model, cold start <br> - Write a Lambda function in Python/Node.js <br> - Configure Lambda triggers: API Gateway, S3, DynamoDB Streams <br> - Set up environment variables and Lambda Layers <br> - Monitor Lambda with CloudWatch Logs and X-Ray | 06/02/2026 | 06/02/2026 | <https://000022.awsstudygroup.com/> |
| Wed | **Lab 17: Remote Server Access with Systems Manager Session Manager** <br> - Study AWS Systems Manager and its features <br> - Configure Session Manager for SSH-less server access <br> - Use SSM Run Command to run commands at scale <br> - Manage Patch Manager for EC2 fleet patching <br> - Store configuration with Parameter Store | 06/03/2026 | 06/03/2026 | <https://000058.awsstudygroup.com/> |
| Thu | **Lab 18: Data Protection with AWS Backup** <br> - Study AWS Backup: Backup Plans, Vaults, Recovery Points <br> - Create an automated Backup Plan for EC2, RDS, EFS, DynamoDB <br> - Configure backup retention and lifecycle policies <br> - Practice restoring from a backup <br> - Set up cross-region backup | 06/04/2026 | 06/05/2026 | <https://000013.awsstudygroup.com/> |
| Fri | - Review and consolidate Week 7 knowledge <br> - Build a small serverless CRUD app: Lambda + API Gateway + DynamoDB <br> - Set up a backup strategy for the entire environment | 06/05/2026 | 06/05/2026 | |

### Week 7 Achievements:

* Developed serverless apps with AWS Lambda:
  * Wrote and deployed Lambda functions handling multiple event types
  * Integrated Lambda with API Gateway to create a RESTful API
  * Connected Lambda to DynamoDB and S3
  * Debugged and monitored Lambda using CloudWatch Logs Insights
  * Understood how to optimize cold start and memory allocation

* Managed systems with AWS Systems Manager:
  * Accessed EC2 securely via Session Manager without opening port 22
  * Ran commands across multiple instances simultaneously
  * Automated OS patching across a server fleet
  * Stored secrets and configuration in Parameter Store

* Established a comprehensive backup strategy:
  * Created automated backup plans with defined schedules
  * Protected multiple resource types: EC2, RDS, DynamoDB
  * Successfully restored from a backup recovery point
  * Configured cross-region backup for disaster recovery
