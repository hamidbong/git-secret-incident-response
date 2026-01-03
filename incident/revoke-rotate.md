
---

## 🔑 Étape 4 – Révocation & rotation

📄 `incident/revoke-rotate.md`

```md
# 🔑 Revoke and Rotate the Secret

Once a secret is exposed, it must be considered compromised.

## Actions
- Revoke the exposed credential
- Generate a new secret
- Update dependent services

## Examples
- API Token → Regenerate from provider
- Cloud Key → Disable & rotate
- Password → Change immediately

❌ Removing the secret from Git is NOT enough.
