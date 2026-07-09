---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---


### Week 5 Objectives:

* Manage authentication security and eliminate hardcoded credentials.
* Remediate storage configuration errors and automatically scan for PII/PHI data.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   |- Credentials Management with AWS Secrets Manager: <br>&emsp; + Understand Secrets Manager architecture <br>&emsp; + Create a Secret for RDS and configure automatic rotation                                                                                             | 18/05/2026   | 18/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 3   |- S3 Security Best Practices: <br>&emsp; + Apply Block Public Access <br>&emsp; + Configure S3 Versioning and Object Lock (Ransomware protection)                                            | 19/05/2026   | 19/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | -Data Protection with Amazon Macie:** <br>&emsp; + Understand PII detection principles using Machine Learning <br>&emsp; + Enable Macie on the account | 20/05/2026   | 20/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | -Setting up Amazon Macie Jobs: <br>&emsp; + Configure Custom Data Identifiers <br>&emsp; + Schedule scans for critical S3 buckets                  | 21/05/2026   | 21/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Lab Practice:** <br>&emsp; + Write code to call the API and retrieve passwords from Secrets Manager <br>&emsp; + Analyze Macie logs regarding data leakage alerts                                                                                         | 22/05/2026   | 22/05/2026      | <https://cloudjourney.awsstudygroup.com/> ||


### Week 5 Achievements:

* Successfully implemented an automated credential rotation process.
* Developed a mechanism for the automated monitoring and detection of sensitive data on S3.
