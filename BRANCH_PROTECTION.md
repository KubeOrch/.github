# Branch Protection Rules

This document describes the branch protection rules applied to KubeOrch repositories.

## Rules Applied to `main` Branch

| Rule | Setting |
|------|---------|
| Require pull request reviews | 1 approval required |
| Dismiss stale reviews | Enabled |
| Allow force pushes | Disabled |
| Allow deletions | Disabled |
| Require conversation resolution | Enabled |

## Repository Status

| Repository | Branch Protection | Notes |
|-----------|------------------|-------|
| docs | Applied | Public repo |
| .github | Applied | Public repo |
| core | Pending | Requires public repo or GitHub Team plan |
| ui | Pending | Requires public repo or GitHub Team plan |
| cli | Pending | Requires public repo or GitHub Team plan |
| community | Pending | Requires public repo or GitHub Team plan |

## Action Required

Branch protection for private repositories (core, ui, cli, community) requires either:

1. **Make repositories public** (recommended before CNCF submission — CNCF projects must be open source)
2. **Upgrade to GitHub Team plan** for the organization

Once repos are made public, apply protection using:

```bash
for repo in core ui cli community; do
  gh api -X PUT "repos/KubeOrch/$repo/branches/main/protection" \
    --input - <<'EOF'
{
  "required_status_checks": null,
  "enforce_admins": false,
  "required_pull_request_reviews": {
    "required_approving_review_count": 1,
    "dismiss_stale_reviews": true
  },
  "restrictions": null,
  "allow_force_pushes": false,
  "allow_deletions": false,
  "required_conversation_resolution": true
}
EOF
done
```
