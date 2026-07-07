---
title: "Week 11 Worklog"
date: 2024-01-01
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Create and deploy 8 Lambda functions with the correct environment variables and SQS trigger.
* Build API Gateway with 8 endpoints, a Cognito Authorizer, and Throttling.
* Create a CloudFront distribution and configure 2 independent WAF Web ACLs (Global + Regional).

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | **Part 7 - Lambda (8 functions)** <br> - Create 8 Lambda functions (Python 3.12), attach `itcoach-lambda-role` <br> - Deploy placeholder code to each function <br> - Set timeout to 30s, memory to 256MB <br> - Configure environment variables for 6 functions: answer-handler, ai-processor, result-handler, session-handler, quiz-handler, gamification-handler | 06/29/2026 | 06/29/2026 | |
| Tue | **Part 7 (cont.) - SQS Trigger + Part 8 - API Gateway** <br> - Attach SQS trigger `itcoach-processing-queue` to `itcoach-ai-processor` (batch size 1) <br> - Create REST API `itcoach-api` (Regional) <br> - Create Cognito Authorizer `itcoach-cognito-auth` <br> - Create 8 resources and methods per the endpoint table <br> - `/auth`: Authorization = NONE; all other 7 endpoints: `itcoach-cognito-auth` <br> - Enable CORS on all resources | 06/30/2026 | 06/30/2026 | |
| Wed | **Part 8 (cont.) + Part 9 - Deploy API + CloudFront** <br> - Deploy API to `prod` stage, save Invoke URL <br> - Configure Throttling: Rate 100 req/s, Burst 200 <br> - Create CloudFront distribution `itcoach-distribution` (Free plan) <br> - Origin: S3 bucket `itcoach-static-assets`, use website endpoint <br> - Default root object: `index.html` <br> - Create 2 custom error responses: 403/404 -> /index.html (200) for React Router | 07/01/2026 | 07/01/2026 | |
| Thu | **Part 10.1 - WAF for CloudFront (Global)** <br> - Confirm CloudFront auto-generated Web ACL `CreatedByCloudFront-...` with 3 default managed rules <br> - Add custom rule `itcoach-rate-limit`: 2000 req / 5 min / IP, Action = Block <br> - Verify rule order: 3 managed rules run before rate-limit <br> **Part 10.2 - WAF for API Gateway (Regional)** <br> - Create Web ACL `itcoach-api-waf` (scope: API Gateway, region ap-southeast-1) <br> - Attach to stage `itcoach-api/prod` <br> - Add 3 managed rule groups + `itcoach-api-rate-limit` (2000/5min) + `itcoach-auth-bruteforce-protect` (20 req / 5 min / IP, scope-down: URI starts with /auth) | 07/02/2026 | 07/03/2026 | |
| Fri | - Verify all Week 11 infrastructure <br> - Test API calls via Invoke URL <br> - Confirm WAF is working: check WAF & Shield console, Requests tab <br> - Verify CloudFront distribution status is Enabled <br> - Prepare for Week 12: Route 53, ACM, real code deployment | 07/03/2026 | 07/03/2026 | |

### Week 11 Achievements:

* Created and fully configured 8 Lambda functions:
  * Attached the correct IAM role `itcoach-lambda-role` to all functions
  * Set environment variables per function (REGION, S3 bucket, DynamoDB tables, SQS URL, OpenAI key)
  * Attached SQS trigger to `itcoach-ai-processor` with batch size 1 for individual message processing
  * Understood the async flow: answer-handler receives request -> pushes to SQS -> ai-processor triggers -> calls OpenAI -> saves result + generates Polly audio

* Built a complete API Gateway:
  * 8 endpoints with correct HTTP methods and Lambda integrations
  * Cognito Authorizer working with JWT from the User Pool
  * `/auth` is public (NONE); all other 7 endpoints require a valid token
  * CORS enabled on all resources
  * Deployed to `prod` stage with Rate 100 / Burst 200 throttling

* Created CloudFront distribution:
  * Origin correctly pointing to the S3 website endpoint
  * Error pages 403/404 redirect to index.html for React Router to work
  * Noted CloudFront domain: `d19z6xk3gva030.cloudfront.net`

* Configured 2 independent WAF Web ACLs:
  * Global WAF (us-east-1): attached to CloudFront, 3 managed rules + 1 custom rate-limit rule
  * Regional WAF (ap-southeast-1): attached to API Gateway prod stage, 3 managed rules + general rate-limit + dedicated `/auth` rule (20 req/5min to prevent brute-force login)
  * Understood why 2 separate WAFs are necessary: the app calls API Gateway directly without going through CloudFront, so the Global WAF cannot filter API traffic
