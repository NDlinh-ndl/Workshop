---
title: "Week 9 Worklog"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Design the concept and architecture for a real-world project: ITCoach.
* Define the tech stack, analyze system requirements, and plan the implementation.
* Design the data model and divide work for the following weeks.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Brainstorm project ideas <br> - Define the core problem: an AI-powered IT interview practice platform <br> - Analyze the target user profile | 06/15/2026 | 06/15/2026 | |
| Tue | - Define tech stack: ReactJS + Lambda + DynamoDB + Cognito + Polly + OpenAI <br> - Design the overall Serverless architecture <br> - Draw the AWS architecture diagram: CloudFront, API Gateway, Lambda, DynamoDB, S3, SQS, Cognito | 06/16/2026 | 06/16/2026 | |
| Wed | - Design data model for 8 DynamoDB tables: <br>&emsp; + itcoach-users, itcoach-questions, itcoach-sessions <br>&emsp; + itcoach-answers, itcoach-history, itcoach-topics <br>&emsp; + itcoach-quiz-attempts (Spaced Repetition SM-2) <br>&emsp; + itcoach-gamification (XP, level, streak, badge) <br> - Define Partition Key, Sort Key, and GSI for each table | 06/17/2026 | 06/17/2026 | |
| Thu | - Design 8 API endpoints: `/auth`, `/questions`, `/topics`, `/sessions`, `/answers`, `/results`, `/quiz`, `/leaderboard` <br> - Analyze the async processing flow: Answer -> SQS -> Lambda AI Processor -> OpenAI -> Polly -> DynamoDB <br> - Plan the security layer: Cognito JWT, WAF, Rate Limiting | 06/18/2026 | 06/19/2026 | |
| Fri | - Create a detailed deployment plan for weeks 10, 11, and 12 <br> - Divide modules: IAM, S3, DynamoDB, Cognito, SQS (week 10) <br> - Lambda, API Gateway, CloudFront, WAF (week 11) <br> - Route 53, ACM, Monitoring, Code deployment (week 12) | 06/19/2026 | 06/19/2026 | |

### Week 9 Achievements:

* Defined the core problem: build an AI-powered IT interview practice platform including Mock Interview (text + voice), a quiz system with Spaced Repetition, and gamification features.

* Designed a complete Serverless architecture on AWS:
  * Frontend: ReactJS hosted on S3, distributed via CloudFront
  * Backend: 8 Lambda functions called through a Regional API Gateway
  * Async processing: SQS -> Lambda AI Processor -> OpenAI STT/GPT -> Polly TTS
  * Auth: Amazon Cognito User Pool with JWT
  * Domain: itcoach24h.xyz, SSL via ACM, DNS via Route 53

* Designed the DynamoDB data model for 8 tables, clearly identifying:
  * Partition Key and Sort Key suited to each access pattern
  * Required GSIs: category-index, userId-index, sessionId-index, xp-index
  * The itcoach-quiz-attempts table stores SM-2 state (interval, easeFactor, nextReviewDate)

* Planned a 2-layer WAF security strategy:
  * Global WAF (us-east-1) attached to CloudFront
  * Regional WAF (ap-southeast-1) attached to API Gateway, with a dedicated rule protecting the `/auth` endpoint against brute-force attacks

* Completed a 3-week deployment plan with clear module assignments based on the ITCoach Console ClickGuide v14.
