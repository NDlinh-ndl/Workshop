---
title: "Week 8 Worklog"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Deploy Kubernetes on AWS with Amazon EKS.
* Build a Data Lake and analyze data with AWS Analytics services.
* Explore Machine Learning on AWS with Amazon SageMaker.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Review Serverless and Operations knowledge from last week <br> - Read Kubernetes concepts: Pod, Deployment, Service, Ingress <br> - Study an overview of Data Analytics on AWS | 06/08/2026 | 06/08/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Tue | **Lab 19: Getting Started with Amazon EKS** <br> - Install and configure eksctl and kubectl <br> - Create an EKS cluster with a managed node group <br> - Deploy an application to EKS using kubectl <br> - Configure ALB Ingress Controller <br> - Set up Horizontal Pod Autoscaler (HPA) <br> - Manage secrets with Kubernetes Secrets and AWS Secrets Manager | 06/09/2026 | 06/09/2026 | <https://000126.awsstudygroup.com/> |
| Wed | **Lab 20: Data Lake Fundamentals on AWS** <br> - Study Data Lake architecture on AWS <br> - Build a Data Lake using Amazon S3 as the storage layer <br> - Use AWS Glue to catalog and ETL data <br> - Query data with Amazon Athena (serverless SQL) <br> - Visualize results with Amazon QuickSight <br> - Explore AWS Lake Formation | 06/10/2026 | 06/10/2026 | <https://000035.awsstudygroup.com/> |
| Thu | **Lab 21: Machine Learning with Amazon SageMaker** <br> - Study SageMaker: Studio, Notebooks, Training Jobs <br> - Launch SageMaker Studio <br> - Prepare and explore a dataset with Jupyter Notebook <br> - Train an ML model with a built-in algorithm (XGBoost) <br> - Deploy the model as a real-time endpoint <br> - Call the endpoint to perform predictions | 06/11/2026 | 06/12/2026 | <https://000200.awsstudygroup.com/> |
| Fri | - Review and consolidate all 7 weeks of lab learning <br> - Draw a complete AWS architecture diagram for a production application <br> - Prepare for Phase 2: ITCoach project design | 06/12/2026 | 06/12/2026 | |

### Week 8 Achievements:

* Deployed applications on Amazon EKS:
  * Created an EKS cluster and managed node groups
  * Deployed, scaled, and updated containerized applications
  * Configured ALB Ingress to expose the application externally
  * Set up HPA to automatically scale pods based on traffic
  * Understood the differences between ECS and EKS and when to use each

* Built a Data Lake and analyzed data:
  * Designed a Data Lake architecture: Raw → Processed → Curated
  * Created a Glue Crawler to automatically catalog data
  * Wrote a Glue ETL job to transform data
  * Queried data with Athena using standard SQL syntax
  * Created a QuickSight dashboard to visualize insights

* Took first steps with Machine Learning on SageMaker:
  * Got familiar with the SageMaker Studio IDE
  * Practiced the full ML workflow: data → train → evaluate → deploy
  * Trained a model with XGBoost on SageMaker managed infrastructure
  * Deployed a model and called the inference endpoint from an application

* **7-week labs summary:**
  * Mastered core AWS services: EC2, VPC, S3, RDS, IAM
  * Capable of designing a 3-tier application architecture on AWS
  * Practiced a complete CI/CD pipeline end-to-end
  * Understood best practices for security, reliability, and performance
  * Completed 21 hands-on labs from foundational to advanced level
