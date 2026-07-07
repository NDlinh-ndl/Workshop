---
title: "Event 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Event Report: FCAJ Community Day (June 27, 2026)

### Event Information

- **Event Name:** FCAJ Community Day
- **Date:** Saturday, June 27, 2026 — 9:00 AM to 12:00 PM (GMT+7)
- **Venue:** Bitexco Financial Tower, Ho Chi Minh City
- **Hosted by:** Huỳnh Hoàng Long
- **Attendance:** 325 people (Sold Out)
- **Event Link:** https://luma.com/s1ymc95q

### Schedule

| Time | Session |
| ---- | ------- |
| 8:30 – 9:00 | Settle in |
| 9:00 – 9:25 | Deep Response Engine: From Detection to Autonomous Resolution |
| 9:25 – 9:55 | Voice Agents: Building Human-Like AI Conversations at Scale |
| 9:55 – 10:20 | AWS DevOps Agent: Your Always-Available Operations Teammate |
| 10:20 – 10:45 | AI-Powered Productivity: Workforce Planning For Enterprise |
| 10:45 – 11:30 | Building Secure Private MCP Connection with Amazon Q |

### Key Session Highlights

#### Deep Response Engine: From Detection to Autonomous Resolution

- The complexity wall in modern cloud operations
- Shifting from alert-driven to action-driven systems
- Deep Response Engine architecture overview
- Live demo: autonomous incident response that detects and resolves issues automatically
- Business impact: cost reduction and zero-downtime operations

#### Voice Agents: Building Human-Like AI Conversations at Scale

- Evolution from IVR and chatbots to AI voice agents
- Core challenges: latency, accuracy, and natural interaction
- **Amazon Nova Sonic**: AWS's new speech-to-speech foundation model
- Architecture: telephony, streaming, Bedrock, MCP tools
- Enterprise use cases, best practices, and live demo

#### AWS DevOps Agent: Your Always-Available Operations Teammate

- Overview of AWS DevOps Agent
- Reducing MTTD (Mean Time to Detect) and MTTR (Mean Time to Resolve) with AI-driven operations
- Supporting multi-cloud and hybrid environments
- **Bedrock AgentCore** and multi-agent reasoning approach
- Real-world use cases and ECS demo walkthrough

#### AI-Powered Productivity: Workforce Planning For Enterprise

- HR transformation challenges in modern enterprises
- Overview of Amazon Q and its HR capabilities
- Accelerating HR operations with automation
- Workforce analytics and data-driven insights
- Strategic workforce planning for enterprise decision-making

#### Building Secure Private MCP Connection with Amazon Q

- Introduction to Amazon Q as an AI assistant platform
- **MCP (Model Context Protocol)** and its role in extensibility
- Security challenges in MCP-based integrations
- Configuring Amazon Q VPC private connectivity
- Demo and real-world implementation insights

### Key Takeaways

**On Autonomous Operations:**
- Deep Response Engine demonstrates the future of cloud operations: systems that detect and resolve incidents automatically without manual intervention, dramatically reducing response time
- The clear distinction between alert-driven (notify only) and action-driven (auto-resolve) represents a fundamental shift in how DevOps teams will operate systems

**On Voice AI:**
- Amazon Nova Sonic is a major advancement in voice AI — processing speech-to-speech instead of the traditional STT → LLM → TTS pipeline, significantly reducing latency
- The voice agent architecture with Bedrock and MCP is directly relevant to ITCoach's Mock Interview feature — currently using Polly but could upgrade to Nova Sonic later

**On DevOps Agent:**
- AWS DevOps Agent with Bedrock AgentCore shows that multi-agent reasoning is the right approach for complex operational problems
- Practical techniques for reducing MTTD/MTTR with AI, immediately applicable to the CloudWatch Alarms system already set up for ITCoach

**On MCP and Security:**
- MCP (Model Context Protocol) is the open standard for connecting AI to external tools — understanding why it is becoming the industry standard
- VPC private connectivity for MCP solves the security problem of AI needing to access internal enterprise data without going through the public internet

### Applying to the ITCoach Project

- Inspired by Deep Response Engine to improve ITCoach monitoring: instead of just creating CloudWatch Alarms for notifications, use Lambda to automatically handle common incidents
- Referenced the Voice Agent architecture with Amazon Nova Sonic to plan an upgrade to the Mock Interview feature — replacing the current Polly TTS pipeline with end-to-end speech-to-speech in a future version
- A better understanding of the MCP protocol informs how ITCoach Lambda functions should communicate with OpenAI and other external services

### Event Experience

This event took place during week 11 of the internship — exactly when I was deploying Lambda and API Gateway for ITCoach. What made it especially relevant was that all 5 talks directly connected to what I was working on: voice AI, DevOps automation, MCP, and security.

The live demo of Deep Response Engine was the standout moment — watching a system automatically detect an ECS failure and trigger a rollback without any human intervention made me rethink how I had designed monitoring for ITCoach.

The event was sold out with 325 attendees. While slightly smaller than the May edition, the talk quality was high and very focused on AI's role in cloud operations — exactly the direction the industry is heading as AI gets embedded into every layer of infrastructure.

### Event Photos

![FCAJ Community Day - June 2026](/images/event21.jpg)
