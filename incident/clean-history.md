# 🧹 Removing Secrets from Git History

## Recommended Tool: git-filter-repo

### Remove a file
```bash
git filter-repo --path .env --invert-paths --force
```

### Step 5: Verify Remediation
```bash
# Scan again to confirm no leaks
gitleaks detect --source . --verbose

    ○
    │╲
    │ ○
    ○ ░
    ░    gitleaks

4:21PM INF 2 commits scanned.
4:21PM INF scan completed in 63.5ms
4:21PM INF no leaks found
```