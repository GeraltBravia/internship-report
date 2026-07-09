---
title: 'Week 11 Worklog'
date: 2026-06-29
weight: 11
chapter: false
pre: ' <b> 1.11. </b> '
---

### Week 11 Objectives:

- Finalize and package automated incident response workflows using AWS Step Functions.
- Expand auto-remediation capabilities: Isolate network resources and disable compromised identities in real-time.
- Standardize audit trails to support digital forensics and compliance.

### Tasks to be carried out this week:

| Day | Task                                                                                                                           | Start Date | Completion Date | Reference Material                          |
| --- | ------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ------------------------------------------- |
| 2   | - Event Orchestration (Workflow Orchestration):** <br>&emsp; + Finalize the State Machine on AWS Step Functions to link conditional processing flows (Choice state). <br>&emsp; + Shift trigger source: Connect EventBridge directly to AWS Security Hub to unify the alert workflow.                    | 29/06/2026   | 29/06/2026      | https://docs.aws.amazon.com/step-functions/ |
| 3   | - Network Containment:** <br>&emsp; + Develop a Lambda function to automatically extract the ID of the malware-infected EC2 instance. <br>&emsp; + Configure a scenario to replace the current Security Group with an "Isolation Security Group" (blocking all Inbound/Outbound traffic except for management ports).                             | 30/06/2026   | 30/06/2026      | https://docs.aws.amazon.com/ec2/            |
| 4   | - Identity Revocation:** <br>&emsp; + Upgrade the Lambda function handling credential compromise incidents. <br>&emsp; + Add logic: Disable Access Keys, revoke active sessions, and block Console Access for the IAM User. | 01/07/2026   | 01/07/2026      | https://docs.aws.amazon.com/iam/            |
| 5   | - Forensic Logging:** <br>&emsp; + Implement logic to generate remediation logs in JSON format. <br>&emsp; + Store logs in Amazon S3 using a time-based directory structure (partitioning) to facilitate querying. <br>&emsp; + Ensure Lambda/Step Functions push comprehensive metrics to CloudWatch.                                    | 02/07/2026   | 02/07/2026      | https://docs.aws.amazon.com/s3/             |
| 6   | - End-to-End Testing:** <br>&emsp; + Inject simulated payloads representing various Security Findings from Security Hub. <br>&emsp; + Verify the entire workflow: Detection -> Rule Trigger -> Step Functions Orchestration -> EC2/IAM Isolation -> SNS Notification -> S3 Log Storage.                         | 03/07/2026   | 03/07/2026      | https://docs.aws.amazon.com/guardduty/      |

### Week 11 Achievements:

- **SOAR Architecture Implementation:** Successfully built a comprehensive incident response orchestration workflow capable of handling conditional branching for specific threat types using AWS Step Functions.
- **Response Time (MTTR) Optimization:** Minimized the time required to isolate compromised EC2 instances and disable IAM access keys from manual intervention to mere seconds.
- **Alert Centralization:** Successfully consolidated event sources, enabling EventBridge to utilize aggregated data directly from AWS Security Hub as the central trigger.
- **Forensics-Ready:** Structured incident response logs are pushed to secure storage (an immutable S3 bucket), ensuring compliance with auditing requirements.
- **Reliable Operations:** End-to-end testing confirmed accurate system performance, with complete execution logs captured in Amazon CloudWatch.