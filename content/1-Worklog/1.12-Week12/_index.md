---
title: "Week 12 Worklog"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives:

- Establish a centralized monitoring hub (Single Pane of Glass) for all security operations.
- Act as Red Team/Blue Team to validate the operational capabilities of the SOC architecture (Detect → Respond → Recover).
- Review privileges, evaluate cost implications, and finalize project handover documentation.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Build a centralized SOC Dashboard: <br>&emsp; + Design Amazon CloudWatch Dashboard. <br>&emsp; + Extract and visualize metrics: GuardDuty Findings, Step Functions Executions, Lambda Errors, EC2 Health.
| 3 | - Configure Alerting Thresholds: <br>&emsp; + Set up CloudWatch Alarms for anomalies (e.g., Lambda error rate > 5%). <br>&emsp; + Validate email notification flows via Amazon SNS triggered by alarms. | 07/07/2026 | 07/07/2026 | https://docs.aws.amazon.com/cloudwatch/ |
| 4 | - Attack & Defense Simulation (Red/Blue Teaming): <br>&emsp; + Execute simulated attack scenarios: EC2 port scanning, IAM Access Key theft. <br>&emsp; + Monitor event flow from Security Hub through to automated threat remediation. | 08/07/2026 | 08/07/2026 | https://docs.aws.amazon.com/guardduty/ |
| 5 | - Privilege Review & Architecture Assessment: <br>&emsp; + Run IAM Access Analyzer to detect over-privileged permissions and tighten access based on the Principle of Least Privilege. <br>&emsp; + Conduct a post-incident review of the Detect → Respond process performance. | 09/07/2026 | 09/07/2026 | https://docs.aws.amazon.com/iam/ |
| 6 | - Acceptance, Handover & Teardown:** <br>&emsp; + Finalize System Architecture Document and Operational Guide. <br>&emsp; + Review costs (Billing) and propose upgrades (IaC, Multi-Account, Amazon Detective). <br>&emsp; + Clean up/tear down resources in AWS accounts to avoid incurring costs. | 10/07/2026 | 10/07/2026 | https://docs.aws.amazon.com/wellarchitected/ |

### Week 12 Achievements:

- **Visual Monitoring:** Successfully deployed a CloudWatch Dashboard acting as a mini-SOC console, displaying real-time critical system metrics (findings, automation metrics, and resource health).
- **Auto-Remediation Validation:** Attack simulation scenarios (Red Teaming) demonstrated the seamless operation of the Detect → Respond → Recover workflow; the system automatically neutralized intrusion attempts within seconds.
- **Access Control Optimization:** Completed the IAM audit, ensuring 100% compliance with the principle of least privilege across all roles and users.
- **Project Documentation Finalization:** Successfully compiled all technical documentation, system diagrams, and operational playbooks. Developed a list of strategic upgrade recommendations (such as Amazon Macie integration and Terraform-based IaC implementation) for future phases.
- **Cost Risk Management (FinOps):** Maintained strict cost control, with all test resources safely decommissioned at the end of the project cycle.