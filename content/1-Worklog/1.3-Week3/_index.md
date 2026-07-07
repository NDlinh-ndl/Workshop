---
title: "Week 3 Worklog"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* Master EC2 — the core compute service of AWS.
* Understand and configure Auto Scaling to ensure high availability.
* Use CloudWatch to monitor resources and set up alerts.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Review VPC knowledge from last week <br> - Read EC2 documentation: instance types, pricing models, AMI <br> - Study EBS volume types and use cases | 05/04/2026 | 05/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Tue | **Lab 4: Compute Essentials with Amazon EC2** <br> - Launch an EC2 instance inside the previously created VPC <br> - Connect via SSH <br> - Attach and mount an EBS volume <br> - Create an AMI from a running instance <br> - Explore Elastic IP | 05/05/2026 | 05/05/2026 | <https://000004.awsstudygroup.com/> |
| Wed | **Lab 5: Scaling Applications with EC2 Auto Scaling** <br> - Learn about Launch Templates <br> - Create an Auto Scaling Group <br> - Configure Scaling Policies (Target Tracking, Step Scaling) <br> - Integrate with Application Load Balancer <br> - Test scale-out and scale-in behavior | 05/06/2026 | 05/06/2026 | <https://000006.awsstudygroup.com/> |
| Thu | **Lab 6: Monitoring with Amazon CloudWatch** <br> - Study CloudWatch Metrics, Logs, Alarms, and Dashboards <br> - Create a CloudWatch Alarm for CPU utilization <br> - Install CloudWatch Agent on EC2 <br> - Build a consolidated Dashboard <br> - Integrate Alarms with Auto Scaling actions | 05/07/2026 | 05/08/2026 | <https://000008.awsstudygroup.com/> |
| Fri | - Review and consolidate Week 3 knowledge <br> - Run a stress test to observe Auto Scaling in action <br> - Write notes on lessons learned | 05/08/2026 | 05/08/2026 | |

### Week 3 Achievements:

* Mastered Amazon EC2:
  * Launched instances with the right instance type per workload
  * Connected via SSH with key pairs and Session Manager
  * Managed EBS volumes: create, attach, mount, resize
  * Created and used AMIs as reusable templates

* Configured a complete Auto Scaling setup:
  * Created a Launch Template with user data script
  * Set up scaling policies based on CPU and request count
  * Integrated with ALB for traffic distribution
  * Observed scale-out under load and scale-in when idle

* Monitored the system with CloudWatch:
  * Created custom metrics via CloudWatch Agent
  * Set up alarms that automatically trigger scaling actions
  * Built a dashboard to track overall system health
