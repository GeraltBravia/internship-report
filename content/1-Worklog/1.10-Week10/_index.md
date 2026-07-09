---
title: 'Week 10 Worklog'
date: 2026-06-22
weight: 10
chapter: false
pre: ' <b> 1.10. </b> '
---

---

### Week 10 Objectives:

- Develop automated incident response workflows (auto-remediation) using a serverless architecture.
- Program automation scripts using AWS Lambda to neutralize threats immediately upon detection.
- Implement an event-driven architecture using Amazon EventBridge and Step Functions to orchestrate incident handling processes.

### Tasks to be carried out this week:

| Day | Task                                                                                                                                                              | Start Date | Completion Date | Reference Material                          |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------------------------------- |
| **2** | - **Alert Channel Configuration:** <br>&emsp; + Deploy an Amazon SNS Topic to serve as the security notification channel. <br>&emsp; + Subscribe project team email addresses and verify the endpoints. | 22/06/2026 | 22/06/2026 | [AWS SNS Docs](https://docs.aws.amazon.com/sns/) |
| **3** | - **Automated Alert Processing (Lambda #1):** <br>&emsp; + Set up an IAM Execution Role with least-privilege permissions. <br>&emsp; + Write a Python script (using Boto3) to parse GuardDuty findings, filter for High/Medium severity alerts, and push the payload to SNS. | 23/06/2026 | 23/06/2026 | [AWS Lambda Docs](https://docs.aws.amazon.com/lambda/) |
| **4** | - **Automated Network Isolation (Lambda #2):** <br>&emsp; + Grant `ec2:AuthorizeSecurityGroupIngress` permissions to the Lambda function. <br>&emsp; + Develop a script to automatically extract the malicious IP from the GuardDuty finding and inject a `Deny` rule into the targeted EC2 instance's Security Group. | 24/06/2026 | 24/06/2026 | [AWS EC2 Docs](https://docs.aws.amazon.com/ec2/) |
| **5** | - **Event Routing:** <br>&emsp; + Configure EventBridge rules to listen for anomalous events from GuardDuty. <br>&emsp; + Trigger the corresponding Lambda function. <br>&emsp; + Inject GuardDuty sample findings to perform end-to-end testing. | 25/06/2026 | 25/06/2026 | [AWS EventBridge Docs](https://docs.aws.amazon.com/eventbridge/) |
| **6** | - **Identity & Orchestration (Lambda #3 & Step Functions):** <br>&emsp; + Develop a script to automatically change the IAM Access Key status to `Inactive` upon suspected exposure. <br>&emsp; + Design a basic State Machine in AWS Step Functions to orchestrate a multi-step workflow. | 26/06/2026 | 26/06/2026 | [AWS Step Functions Docs](https://docs.aws.amazon.com/step-functions/) |

### Week 10 Achievements:

- **Real-time Alerting System:** Successfully established an emergency email notification workflow by integrating EventBridge and Amazon SNS.
- **Threat Containment (Network Containment):** Successfully deployed a Lambda function to automatically modify EC2 Security Groups, instantly blocking connections to C&C (Command & Control) IPs or network scanning sources.
- **Identity Protection (Identity Revocation):** Finalized a Python 3.12 script to automatically revoke IAM Access Keys, mitigating the risk of Account Takeover.
- **Event-Driven Architecture (Event-Driven Security):** Standardized event routing via Amazon EventBridge, ensuring a latency of only a few seconds between GuardDuty detection and Lambda execution.
- **Secure Coding Practices:** Strictly adhered to the Principle of Least Privilege using IAM Roles; implemented comprehensive exception handling (try/except) in Lambda source code and maintained transparent execution logs in CloudWatch Logs.
- **SOAR Readiness:** Successfully laid the groundwork for orchestrating complex incident response workflows using AWS Step Functions.
