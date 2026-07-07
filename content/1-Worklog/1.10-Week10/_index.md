---
title: "Week 10 Worklog"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Set up the base AWS infrastructure for the ITCoach project: IAM, S3, DynamoDB, Cognito, SQS.
* Create all 8 DynamoDB tables with the correct key schema and GSIs as designed.
* Complete the base infrastructure, ready for Lambda and API Gateway in the next week.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | **Part 1 - IAM Role** <br> - Create IAM Role `itcoach-lambda-role` <br> - Attach 6 managed policies: AWSLambdaBasicExecutionRole, AmazonDynamoDBFullAccess, AmazonS3FullAccess, AmazonSQSFullAccess, AmazonPollyFullAccess, CloudWatchFullAccess | 06/22/2026 | 06/22/2026 | |
| Tue | **Part 2 + 3 - S3 Buckets** <br> - Create `itcoach-static-assets` bucket (public, static website hosting: index.html) <br> - Create `itcoach-audio-upload` bucket (private, configure CORS to allow GET/PUT/POST/DELETE) | 06/23/2026 | 06/23/2026 | |
| Wed | **Part 4 - DynamoDB (8 tables, On-demand)** <br> - Create 8 tables: users, questions, sessions, answers, history, topics, quiz-attempts, gamification <br> - Create GSIs: category-index (questions), userId-index (sessions), sessionId-index (answers), xp-index (gamification: type+xp) <br> - topics table: PK=specialty, SK=topicId <br> - quiz-attempts table: PK=userId, SK=questionId <br> - history table: PK=userId, SK=timestamp | 06/24/2026 | 06/24/2026 | |
| Thu | **Part 5 + 6 - Cognito + SQS** <br> - Create Cognito User Pool, App Client `itcoach-web-client` (SPA), sign-in via Email, required attribute: name <br> - Save User Pool ID and App Client ID <br> - Create SQS DLQ `itcoach-dlq` first <br> - Create main queue `itcoach-processing-queue`: visibility timeout 300s, encryption enabled, attach DLQ (max receives 3) <br> - Save the Queue URL | 06/25/2026 | 06/26/2026 | |
| Fri | - Verify all Week 10 infrastructure <br> - Confirm all 8 DynamoDB tables have the correct key schema and GSIs <br> - Test Cognito sign-up/sign-in <br> - Prepare a list of saved values needed for Week 11 | 06/26/2026 | 06/26/2026 | |

### Week 10 Achievements:

* Successfully created IAM Role `itcoach-lambda-role` with all 6 required permissions for all Lambda functions.

* Set up 2 S3 buckets with the correct configuration:
  * `itcoach-static-assets`: public access, static website hosting enabled, index/error document = index.html
  * `itcoach-audio-upload`: private, CORS policy allowing browser-based audio uploads

* Created all 8 DynamoDB tables with On-demand capacity mode:
  * Defined the correct Partition Key and Sort Key for each access pattern
  * Created 4 GSIs: category-index, userId-index, sessionId-index, xp-index (type String + xp Number)
  * Understood the design reasoning: the gamification table uses `type="USER"` to group all users into one partition, sorted by xp for the leaderboard

* Configured Cognito User Pool:
  * App type: Single-page application (SPA)
  * Sign-in: Email
  * Required attribute: name
  * Saved User Pool ID (`ap-southeast-1_Z4aYtoxGr`) and App Client ID

* Created SQS queues in the correct order (DLQ first, then main queue):
  * DLQ: `itcoach-dlq`
  * Main queue: `itcoach-processing-queue`, visibility 300s, encryption enabled, DLQ attached with max 3 retries
  * Saved Queue URL for Lambda environment variable configuration next week
