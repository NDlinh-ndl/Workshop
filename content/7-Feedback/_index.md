---
title: "Sharing and Feedback"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 7. </b> "
---

### Overall Evaluation

**1. Learning and Working Environment**

The First Cloud Journey - AWS Study Group environment is open and highly practical. The entire program is designed around hands-on learning — not just reading theory, but actually working on the AWS Console, debugging real errors, and finding solutions independently.

What impressed me most was the community atmosphere: everyone shares real-world experience, supports each other through the group, and no one gets left behind when facing technical difficulties. The two FCAJ Community Day events at Bitexco in May and June 2026 also gave me the opportunity to connect with the broader AWS Vietnam community.

**2. Support from Mentors and the Community**

The guides on cloudjourney.awsstudygroup.com are very well-prepared, with step-by-step screenshots that are easy to follow even when the AWS interface changes. When I encountered errors not covered in the documentation — like WAF blocking valid requests, stale CloudFront cache, or SQS triggers not firing — I had to investigate through CloudWatch Logs and AWS documentation myself. This actually helped me learn far more deeply than just following a guide.

The AWS Study Group Facebook community was also an important support resource for specific technical questions.

**3. Relevance to Real-World Careers**

The 12-week roadmap is well-structured: 8 weeks learning core AWS services through 21 progressively ordered labs, then 4 weeks applying that knowledge to a real project. This approach helped me not only understand each service individually but also see how to combine them into a complete system.

The ITCoach project was where I learned the most: from designing a Serverless architecture, selecting the right AWS service for each problem, handling real deployment issues, to managing costs and securing a production system.

**4. Learning and Skill Development Opportunities**

After 12 weeks, I was able to:
- Design and deploy a Serverless architecture from scratch on AWS
- Write and debug Lambda functions, configure API Gateway with Cognito auth
- Design a DynamoDB data model for a real application
- Configure CloudFront, WAF, Route 53, and ACM
- Read CloudWatch Logs to trace production errors
- Manage AWS costs and identify services that can unexpectedly exceed budget

These are skills I could not have gained from textbooks or typical online courses alone.

**5. Community Culture**

FCAJ has a positive sharing culture. The Community Days were not just lecture sessions — they were a chance to see how experienced engineers actually use AWS in their daily work, from autonomous incident response to voice AI, multi-agent systems to MCP security. This gave me a much clearer picture of what I was learning and where I would apply it.

**6. Program Structure and Curriculum**

The curriculum scales in difficulty at a reasonable pace. That said, 21 labs in 8 weeks is quite dense — averaging 3 labs per week, each requiring 1-2 hours to read, complete, and understand. The early weeks were slower as I was still getting familiar with the AWS Console. I think allocating more time for complex labs like EKS and SageMaker would allow for deeper learning rather than rushing to keep up with the schedule.

---

### Most Satisfying Moment

Completing the ITCoach project and seeing the website live at `https://itcoach24h.xyz` with HTTPS, WAF protection, and CloudWatch monitoring — everything I built from week 9 to week 12. This was not a demo or mockup, but a real system running on AWS.

### What the Program Should Improve

The documentation for some labs has not been updated to match the latest AWS Console UI — especially Cognito (the new interface is completely different from the old wizard) and CloudFront (the distribution creation workflow has changed). I spent significant time cross-referencing the old docs with the new interface to find the right options.

### Would You Recommend It to Friends?

Yes, especially for those pursuing Cloud Engineer, DevOps, or Backend Developer roles with AWS experience. The program provides hands-on experience that typical certification courses simply cannot replicate.

### Suggestions

- Update screenshots in the lab guides to reflect the latest AWS Console UI
- Add a "Common Errors & Troubleshooting" section to each lab covering frequent issues and how to resolve them
- Consider extending the project phase (weeks 9-12) by 1-2 weeks to allow more time for refinement and thorough testing
- Organize a demo day at the end of the program where participants can present their projects to the community
