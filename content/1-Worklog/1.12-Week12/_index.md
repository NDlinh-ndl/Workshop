---
title: "Week 12 Worklog"
date: 2024-01-01
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives:

* Configure Route 53, purchase a domain, and attach an SSL Certificate via ACM.
* Set up SNS and CloudWatch Alarms for system monitoring.
* Build and deploy real code (ReactJS + 8 Lambda), confirm the website is live at itcoach24h.xyz.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | **Part 11 - SNS + CloudWatch** <br> - Create SNS Topic `itcoach-alerts` (Standard) <br> - Create Email subscription and confirm via email <br> - Create 3 CloudWatch Alarms: <br>&emsp; + `itcoach-ai-errors`: Lambda itcoach-ai-processor Errors > 5 / 5 min <br>&emsp; + `itcoach-api-5xx-errors`: API Gateway 5XXError > 10 / 5 min <br>&emsp; + `itcoach-sqs-backlog`: SQS ApproximateNumberOfMessagesVisible > 50 / 5 min <br> - Attach all 3 alarms to SNS topic `itcoach-alerts` | 07/06/2026 | 07/06/2026 | |
| Tue | **Part 12 - Route 53 + ACM** <br> - Purchase domain `itcoach24h.xyz` on Namecheap (enable Free Domain Privacy, disable Auto-renew) <br> - Create Hosted Zone `itcoach24h.xyz` (Public) on Route 53, copy 4 NS records to Namecheap Custom DNS <br> - Switch Region to us-east-1 (N. Virginia) <br> - Request SSL Certificate on ACM: `itcoach24h.xyz` + `*.itcoach24h.xyz`, DNS validation, create records in Route 53 <br> - Wait for Certificate status to change to Issued | 07/07/2026 | 07/07/2026 | |
| Wed | **Part 12 (cont.) - Attach domain to CloudFront + DNS Records** <br> - Switch Region back to ap-southeast-1 <br> - In CloudFront `itcoach-distribution`: add CNAMEs `itcoach24h.xyz` and `www.itcoach24h.xyz`, attach the SSL certificate <br> - Create 2 Alias A records in Route 53 pointing to the CloudFront distribution: root domain and www <br> - Wait for DNS propagation, access `https://itcoach24h.xyz` to verify | 07/08/2026 | 07/08/2026 | |
| Thu | **Deploy real code** <br> - Frontend: run `npm run build`, upload entire `/dist` to S3 bucket `itcoach-static-assets`, create CloudFront Invalidation (`/*`) <br> - Backend: package 8 Lambda functions into `.zip` files, upload to each function via console <br> - Update Cognito Callback URL from `localhost:3000` to `https://itcoach24h.xyz` <br> - Test full user flow: sign up -> sign in -> quiz -> mock interview -> leaderboard | 07/09/2026 | 07/10/2026 | |
| Fri | - Final end-to-end system verification <br> - Confirm 12/12 infrastructure parts are complete <br> - Insert sample data into `itcoach-questions` and `itcoach-topics` <br> - Review CloudWatch Alarms and WAF logs <br> - Write project summary and draw the final architecture diagram | 07/10/2026 | 07/10/2026 | |

### Week 12 Achievements:

* Set up system monitoring with SNS + CloudWatch:
  * SNS topic `itcoach-alerts` sends email notifications when incidents occur
  * 3 alarms cover the 3 most critical points: Lambda errors, API 5xx, SQS backlog
  * Understood that "Insufficient data" status is normal before real traffic exists

* Completed domain and SSL configuration:
  * Purchased and pointed domain `itcoach24h.xyz` from Namecheap to Route 53 (4 NS records)
  * Created a wildcard SSL Certificate (`*.itcoach24h.xyz`) on ACM us-east-1 with DNS validation
  * Attached the certificate to CloudFront, created 2 Alias A records (root + www) pointing to CloudFront

* Deployed real code and confirmed the system is operational:
  * ReactJS built successfully, uploaded to S3, CloudFront Invalidation to clear cache
  * 8 Lambda functions running real code (handling quiz, mock interview, gamification)
  * Website accessible at `https://itcoach24h.xyz` with HTTPS

* Completed all 12/12 AWS infrastructure parts:
  * Stack: Serverless - ReactJS + Lambda + DynamoDB + Cognito + Polly + OpenAI + WAF (CloudFront + API Gateway)
  * Region: ap-southeast-1 (Singapore) | Domain: itcoach24h.xyz
  * API Gateway URL: `https://shyhx5tj6k.execute-api.ap-southeast-1.amazonaws.com/prod`
  * 2 independent WAF Web ACLs protecting both CloudFront and API Gateway
  * Total: 8 Lambda functions, 8 DynamoDB tables, 8 API endpoints, 2 S3 buckets, 1 Cognito User Pool, 2 SQS queues, 2 WAF Web ACLs, 3 CloudWatch Alarms
