---
title: "Week 5 Worklog"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Configure Route 53 for DNS management and routing policies.
* Protect web applications with AWS WAF.
* Encrypt data with AWS Key Management Service (KMS).

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Review Storage and Database knowledge from last week <br> - Read documentation on basic DNS and record types <br> - Study AWS Security best practices overview | 05/18/2026 | 05/18/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Tue | **Lab 10: Hybrid DNS Management with Amazon Route 53** <br> - Study Route 53: Hosted Zones, Record Types <br> - Configure Routing Policies: Simple, Weighted, Latency, Failover, Geolocation <br> - Integrate Route 53 with ALB and CloudFront <br> - Set up Health Checks <br> - Practice DNS failover scenarios | 05/19/2026 | 05/19/2026 | <https://000010.awsstudygroup.com/> |
| Wed | **Lab 11: Application Protection with AWS WAF** <br> - Study WAF: Web ACL, Rules, Rule Groups <br> - Create a Web ACL with AWS Managed Rules <br> - Write custom rules to block/allow traffic <br> - Attach WAF to ALB and CloudFront <br> - Analyze WAF logs in CloudWatch | 05/20/2026 | 05/20/2026 | <https://000026.awsstudygroup.com/> |
| Thu | **Lab 12: Encryption with AWS Key Management Service (KMS)** <br> - Study KMS: CMK, Data Key, Envelope Encryption <br> - Create a KMS key and configure key policy <br> - Encrypt EBS volumes and S3 buckets with KMS <br> - Encrypt RDS database <br> - Use KMS with AWS CLI | 05/21/2026 | 05/22/2026 | <https://000033.awsstudygroup.com/> |
| Fri | - Review and consolidate Week 5 knowledge <br> - Design a complete security architecture for a web application <br> - Write notes on AWS Security best practices | 05/22/2026 | 05/22/2026 | |

### Week 5 Achievements:

* Configured Route 53 proficiently:
  * Created hosted zones and managed DNS records
  * Configured 5+ different routing policy types
  * Set up health checks and automatic DNS failover
  * Understood how Route 53 integrates with other AWS services

* Protected applications with AWS WAF:
  * Created Web ACLs with managed rule groups
  * Wrote custom rules to handle specific threats
  * Analyzed and investigated WAF logs
  * Understood common attack types: SQL injection, XSS, DDoS

* Managed encryption with KMS:
  * Created and managed Customer Managed Keys
  * Applied at-rest encryption to EBS, S3, and RDS
  * Understood envelope encryption mechanics
  * Configured automatic key rotation
