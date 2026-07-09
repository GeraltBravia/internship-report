---
title: 'Week 9 Worklog'
date: 2026-06-15
weight: 9
chapter: false
pre: ' <b> 1.9. </b> '
---

### Week 9 Objectives:

- Build a security monitoring foundation for the project's entire cloud infrastructure.
- Implement automation for log collection, threat detection, and resource alerting.

### Tasks to be carried out this week:

| Day | Task                                                                                                                                                                             | Start Date | Completion Date | Reference Material                       |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ---------------------------------------- |
| 2   | - Establish Security Baseline:** <br>&emsp; + Create the project AWS account and enable MFA for the Root User. <br>&emsp; + Configure administrative permissions via IAM Groups and provision an IAM User (with AdministratorAccess) for daily operations instead of using the Root User.                                                                      | 15/06/2026   | 15/06/2026      | https://docs.aws.amazon.com/iam/         |
| 3   | - Implement Logging & Networking Visibility:** <br>&emsp; + Configure AWS CloudTrail to audit all API calls. <br>&emsp; + Enable VPC Flow Logs to analyze network traffic and export data centrally to Amazon CloudWatch Logs.                                                                         | 16/06/2026   | 16/06/2026      | https://docs.aws.amazon.com/cloudtrail/  |
| 4   | - Compliance & Budget Monitoring (FinOps):** <br>&emsp; + Set up AWS Config to continuously track and evaluate resource configuration changes. <br>&emsp; + Configure AWS Budgets and route monthly cost alerts (Cost Alarms) to control resources.                                                              | 17/06/2026   | 17/06/2026      | https://docs.aws.amazon.com/config/      |
| 5   | - Centralized Threat Detection:** <br>&emsp; + Enable Amazon GuardDuty (region ap-southeast-1) for intelligent log analysis. <br>&emsp; + Deploy AWS Security Hub, apply the NIST 800-53 standard, and synchronize GuardDuty findings to a single dashboard.                           | 18/06/2026   | 18/06/2026      | https://docs.aws.amazon.com/securityhub/ |
| 6   | - Automated Testing & Alerting:** <br>&emsp; + Launch IAM Access Analyzer to review external sharing policies (Cross-account/Public). <br>&emsp; + Create CloudWatch Alarms to monitor failed login events and Root account usage. <br>&emsp; + Generate GuardDuty sample findings to verify the alert flow in Security Hub. | 19/06/2026   | 19/06/2026      | https://docs.aws.amazon.com/guardduty/ |

### Week 9 Achievements:

**Identity & Access Security:** Strengthened the first line of defense by implementing MFA and an IAM User/Group architecture that adheres to the principle of Least Privilege.
- **Comprehensive Log Collection & Analysis:** Ensured system traceability by successfully configuring CloudTrail (for API activities) and VPC Flow Logs (for network traffic).
- **Budget Control & Compliance:** Successfully established resource configuration monitoring (AWS Config) and automated alerting mechanisms for cost threshold breaches (AWS Budgets).
- **Threat Detection:** Deployed Amazon GuardDuty to ensure the capability to detect anomalous activities, such as scanning and intrusion attempts.
- **Centralized Security Management:** Successfully consolidated risk alerts into AWS Security Hub, meeting security assessment requirements based on the NIST 800-53 standard.
- **Alerting System Validation:** Verified that CloudWatch Alarms respond accurately to test scenarios (GuardDuty Sample Findings and Failed Logins), ensuring readiness for automated incident response in the coming weeks.