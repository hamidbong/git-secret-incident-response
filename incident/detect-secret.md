# 🔍 Detecting a Leaked Secret

Secrets may be detected by:
- GitGuardian alerts
- CI/CD secret scanning
- Manual audit: Gitleaks

Gitleaks blocks secrets before they reach production,
GitGuardian monitors and manages incidents at scale.
## Example with Gitleaks

### Step 1: Create a Test File with Secrets
Create a test file to simulate leaked secrets:

```bash
# Create a test file with a fake AWS key
echo 'AWS_ACCESS_KEY_ID=AKIAIOSFODNN7EXAMPLE' > test-secrets.env
echo 'AWS_SECRET_ACCESS_KEY=wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY' >> test-secrets.env
git add test-secrets.env
git commit -m "Added configuration file"
```

### Step 2: Detect Secrets with gitleaks

Install gitleaks tools for detecting:

```bash
sudo apt install gitleaks
```

Run gitleaks to scan for secrets:

```bash
gitleaks detect --source . --verbose
```

**Expected output when secrets are found:**
```
   ○
    │╲
    │ ○
    ○ ░
    ░    gitleaks

Finding:     AWS_ACCESS_KEY_ID=AKIAIOSFODNN7EXAMPLE
Secret:      AKIAIOSFODNN7EXAMPLE
RuleID:      aws-access-token
Entropy:     3.684184
File:        test-secrets.env
Line:        1
Commit:      e0ed2a671559dfd979b10f1d7714aa4f26ba3fe0
Author:      brahim bong
Email:       brahbong@gmail.com
Date:        2026-01-03T15:02:20Z
```


