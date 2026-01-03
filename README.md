# 🔐 Git Secret Incident Response (DevSecOps)

This repository demonstrates a real-world DevSecOps incident:
**a secret accidentally pushed to a Git repository**.

## 🎯 Objectives
- Detect exposed secrets
- Revoke and rotate compromised credentials
- Remove secrets from Git history
- Implement preventive security controls

## 🛠 Tools
- GitGuardian (continuous monitoring & incident management)
- Gitleaks (local or CI/CD secret scanning)
- Git
- Pre-commit hooks

## 📚 Repository Structure
See `/incident` for step-by-step remediation.

## 🧠 Key DevSecOps Takeaway

Security cannot rely on a single control.

- Gitleaks prevents secrets from entering the repository
- GitGuardian detects and manages incidents at scale


## ❌ Common Bad Practices (What NOT to Do)

The following practices frequently lead to security incidents
and secret leaks in Git repositories:

- Committing `.env` or configuration files containing secrets
- Hardcoding API keys, tokens, or credentials in source code
- Sharing sensitive information directly in commits
- Ignoring security alerts and secret scanning warnings

⚠️ Each of these practices significantly increases the risk
of infrastructure compromise and data breaches.


## 🔄 DevSecOps Secret Detection & Incident Response Flow

[![DevSecOps Flow](images/devsecops-secret-flow.png)](images/devsecops-secret-flow.png)

This diagram illustrates a defense-in-depth approach.

**Defense in depth is mandatory.**

## 🔗 Portfolio
This project is part of my DevSecOps portfolio.