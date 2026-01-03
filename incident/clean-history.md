# 🧹 Removing Secrets from Git History

## Recommended Tool: git-filter-repo

### Remove a file
```bash
git filter-repo --path .env --invert-paths
