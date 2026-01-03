# 🛡️ GitGuardian Integration Guide

GitGuardian is used in this project to monitor repositories
and detect secrets in real time after commits are pushed.

## 🔌 Repository Connection
1. Create a GitGuardian account
2. Connect GitHub / GitLab
3. Enable repository monitoring
4. Activate pull request scanning

## 🔔 Alerts & Incidents
When a secret is detected:
- An alert is generated instantly
- The secret is classified by type
- Validity is checked automatically
- A remediation workflow is suggested

## 🧯 Incident Handling Workflow
1. Revoke or rotate the exposed secret
2. Clean Git history if required
3. Close the incident in GitGuardian
4. Monitor for recurrence

> GitGuardian focuses on detection, visibility, and response,
> not on blocking commits.
