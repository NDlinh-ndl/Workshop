---
title: "Week 6 Worklog"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Automate infrastructure with AWS CloudFormation (Infrastructure as Code).
* Build a CI/CD pipeline with AWS CodePipeline.
* Containerize applications with Docker and deploy to Amazon ECS.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Review Networking and Security knowledge from last week <br> - Read documentation on Infrastructure as Code (IaC) concepts <br> - Study CI/CD and DevOps practices | 05/25/2026 | 05/25/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Tue | **Lab 13: Infrastructure as Code with AWS CloudFormation** <br> - Study CloudFormation: Templates, Stacks, Change Sets <br> - Write a CloudFormation template to create VPC + EC2 + RDS <br> - Use Parameters, Mappings, Conditions, and Outputs <br> - Update a stack using Change Sets <br> - Practice stack rollback on deployment failure | 05/26/2026 | 05/26/2026 | <https://000037.awsstudygroup.com/> |
| Wed | **Lab 14: CI/CD Pipeline with AWS CodePipeline** <br> - Study CodeCommit, CodeBuild, CodeDeploy, CodePipeline <br> - Create a repository on CodeCommit <br> - Configure CodeBuild to build and test the application <br> - Create a pipeline to auto-deploy to EC2 <br> - Trigger the pipeline on code push | 05/27/2026 | 05/27/2026 | <https://000017.awsstudygroup.com/> |
| Thu | **Lab 15: Containerization with Docker and Amazon ECS** <br> - Install Docker and build a Docker image <br> - Push the image to Amazon ECR <br> - Create an ECS Cluster (Fargate) <br> - Create a Task Definition and Service <br> - Configure ALB with ECS service <br> - Update container image via rolling deployment | 05/28/2026 | 05/29/2026 | <https://000016.awsstudygroup.com/> |
| Fri | - Review and consolidate Week 6 knowledge <br> - Connect CodePipeline with ECS to create a full end-to-end pipeline <br> - Compare deploying on EC2 vs ECS | 05/29/2026 | 05/29/2026 | |

### Week 6 Achievements:

* Wrote CloudFormation templates proficiently:
  * Created a multi-tier architecture (VPC + EC2 + RDS) as code
  * Used Parameters to build reusable templates
  * Safely performed stack updates via Change Sets
  * Understood the full lifecycle of a CloudFormation stack

* Built a CI/CD pipeline with CodePipeline:
  * Set up a 3-stage pipeline: Source → Build → Deploy
  * Configured CodeBuild with a buildspec.yml file
  * Automatically deployed to EC2 on every new commit
  * Added a manual approval step before deploying to production

* Deployed containers to Amazon ECS:
  * Built and pushed Docker images to ECR
  * Created an ECS service running on Fargate (serverless)
  * Configured health checks and auto-recovery
  * Performed zero-downtime rolling deployments
