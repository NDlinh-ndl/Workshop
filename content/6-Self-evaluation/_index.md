---
title: "Self-Assessment"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

During my internship at **First Cloud Journey - AWS Study Group** from **08/11/2025** to **10/24/2025**, I had the opportunity to learn, practice, and apply AWS knowledge to a real-world project.

In the first 8 weeks (weeks 2–8), I focused on studying and completing 21 hands-on labs on cloudjourney.awsstudygroup.com, progressing from foundational services like IAM, VPC, and EC2 to advanced topics such as EKS, Serverless, Data Lake, and SageMaker. Over the following 4 weeks (weeks 9–12), I designed and fully deployed the **ITCoach** project — an AI-powered IT interview practice platform — on a Serverless AWS architecture, including 8 Lambda functions, 8 DynamoDB tables, API Gateway, CloudFront, WAF, Cognito, SQS, Route 53, and ACM. The website is currently live at https://itcoach24h.xyz.

Throughout the internship, I not only improved my technical AWS skills but also developed system design thinking, documentation habits, and the ability to independently troubleshoot real-world issues.

To objectively reflect on my internship period, I would like to evaluate myself based on the following criteria:

| No. | Criteria | Description | Good | Fair | Average |
| --- | -------- | ----------- | ---- | ---- | ------- |
| 1 | **Professional knowledge & skills** | Completed 21 AWS labs; successfully designed and deployed the full ITCoach system (12 parts) on AWS Serverless | ✅ | ☐ | ☐ |
| 2 | **Ability to learn** | Quickly absorbed AWS services from basic to advanced; independently researched beyond the provided materials when facing real-world issues | ✅ | ☐ | ☐ |
| 3 | **Proactiveness** | Self-organized a weekly learning plan; proactively proposed the ITCoach idea and architecture without waiting for instructions | ✅ | ☐ | ☐ |
| 4 | **Sense of responsibility** | Completed all planned tasks each week; real code was built and deployed, and the system runs stably | ✅ | ☐ | ☐ |
| 5 | **Discipline** | Generally followed the study schedule and plan; occasionally delayed on minor tasks | ☐ | ✅ | ☐ |
| 6 | **Progressive mindset** | Willing to revisit and fix mistakes; self-debugged Lambda errors, WAF false-positives, and CloudFront misconfigurations | ✅ | ☐ | ☐ |
| 7 | **Communication** | Able to present system architecture and weekly worklogs clearly; technical English writing still needs improvement | ☐ | ✅ | ☐ |
| 8 | **Teamwork** | Actively engaged in the AWS Study Group community; shared experiences when encountering real-world errors | ✅ | ☐ | ☐ |
| 9 | **Professional conduct** | Maintained respect for the learning environment; kept a positive attitude when facing technical difficulties | ✅ | ☐ | ☐ |
| 10 | **Problem-solving skills** | Resolved real issues: WAF blocking valid requests, CORS errors, Lambda timeouts, SQS messages not being consumed; though sometimes took too long to identify the root cause | ☐ | ✅ | ☐ |
| 11 | **Contribution to project** | Solely designed the architecture and built the entire ITCoach infrastructure end-to-end; the product runs on a real domain | ✅ | ☐ | ☐ |
| 12 | **Overall** | Achieved the internship goals: mastered AWS and built a real-world product from design to production | ✅ | ☐ | ☐ |

### Strengths

* Strong ability to absorb technical knowledge quickly and apply it in practice within the same week of studying.
* Good systems thinking: able to design architectures suited to the actual problem rather than just following pre-existing templates.
* Persistent when facing technical errors — did not give up when WAF blocked valid requests, SQS failed to trigger, or CloudFront served stale cache.
* Security-minded from the design phase: separated WAF into 2 independent layers, applied a stricter rate-limit specifically for the sensitive `/auth` endpoint.

### Areas for Improvement

* Time discipline: need to follow deadlines more strictly and avoid letting small tasks pile up toward the end of the week.
* Technical English writing: need to improve the ability to present and document technical content in clear, professional English.
* Systematic debugging: instead of trial-and-error, need to develop the habit of reading CloudWatch Logs and tracing errors from the root cause faster.
* Cost awareness: need to pay more attention to cost implications when designing systems, especially when using request-based billing services like WAF.
