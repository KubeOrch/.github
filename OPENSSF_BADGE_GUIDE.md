# OpenSSF Best Practices Badge — Self-Certification Guide

This guide walks through obtaining the OpenSSF Best Practices "passing" badge for KubeOrch.

## Step 1: Register the Project

1. Go to https://www.bestpractices.dev/
2. Click "Get Your Badge Now!"
3. Log in with GitHub
4. Enter the repository URL: `https://github.com/KubeOrch/core`
5. Begin the self-certification questionnaire

## Step 2: Pre-Filled Answers

Below are the answers based on KubeOrch's current state. Use these when filling out the questionnaire.

### Basics

| Question | Answer | Evidence |
|----------|--------|----------|
| OSS license | Apache-2.0 | `LICENSE` file in all repos |
| Project website | Yes | https://docs.kubeorch.dev |
| Description in natural language | Yes | README.md in all repos |
| How to contribute | Yes | [CONTRIBUTING.md](https://github.com/KubeOrch/.github/blob/main/CONTRIBUTING.md) |
| Project oversight / governance | Yes | [GOVERNANCE.md](https://github.com/KubeOrch/.github/blob/main/GOVERNANCE.md) |

### Change Control

| Question | Answer | Evidence |
|----------|--------|----------|
| Public version-control repository | Yes | GitHub repos under KubeOrch org |
| Unique version numbering | Yes | Semver (see [RELEASE_PROCESS.md](https://github.com/KubeOrch/community/blob/main/RELEASE_PROCESS.md)) |
| Release notes | Pending | CHANGELOG.md to be added per release process |

### Reporting

| Question | Answer | Evidence |
|----------|--------|----------|
| Bug reporting process | Yes | GitHub Issues with templates |
| Vulnerability reporting process | Yes | [SECURITY.md](https://github.com/KubeOrch/.github/blob/main/SECURITY.md) |

### Quality

| Question | Answer | Evidence |
|----------|--------|----------|
| Working build system | Yes | Go build, Next.js build, CI pipelines |
| Automated test suite | Yes | GitHub Actions CI on all repos |
| Tests added for new functionality | Yes (policy) | Required in CONTRIBUTING.md |
| Warning flags enabled | Yes | golangci-lint (28+ linters), ESLint with TypeScript |

### Security

| Question | Answer | Evidence |
|----------|--------|----------|
| Secure development knowledge | Yes | Security practices in CONTRIBUTING.md |
| Secure design principles | Yes | Non-root containers, AES-GCM encryption, bcrypt hashing |
| Input validation | Yes | Gin request binding, Zod form validation |
| Cryptographic practices | Yes | bcrypt for passwords, AES-GCM for secrets, JWT for tokens |

### Analysis

| Question | Answer | Evidence |
|----------|--------|----------|
| Static analysis | Yes | golangci-lint, ESLint, gosec |
| Dynamic analysis | Partial | Trivy security scanning in CI |

## Step 3: After Registration

1. Complete the questionnaire using the answers above
2. Submit for "passing" level
3. Copy the badge URL
4. Add the badge to all repository READMEs:

```markdown
[![OpenSSF Best Practices](https://www.bestpractices.dev/projects/XXXXX/badge)](https://www.bestpractices.dev/projects/XXXXX)
```

Replace `XXXXX` with the project number assigned after registration.

## Step 4: Track Progress

Some items may need improvement to reach "passing":
- Ensure CHANGELOG.md exists and is updated with each release
- Increase test coverage (target: 40%+ for core, 30%+ for UI)
- Add dynamic analysis tooling if not yet sufficient

Review the badge status periodically and address any gaps.
