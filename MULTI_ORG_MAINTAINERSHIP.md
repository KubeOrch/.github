# Multi-Organization Maintainership Plan

## Current State

KubeOrch currently has 4 core maintainers, all from the founding team. For CNCF sandbox acceptance, the project needs a credible path toward multi-organization maintainership.

## Goal

Attract at least 1-2 maintainers from external organizations within 6 months of CNCF sandbox acceptance.

## Strategy

### Phase 1: Lower the Barrier (Before CNCF Application)

**Good First Issues**
- Maintain a steady pipeline of `good-first-issue` labeled issues across all repos
- Include clear descriptions, expected approach, and relevant file pointers
- Respond to new contributors within 48 hours

**Documentation for Contributors**
- Ensure CONTRIBUTING.md is beginner-friendly
- Add architecture guides that help newcomers understand the codebase
- Document local development setup with one-command start

**Welcoming Community**
- Acknowledge all contributions (issues, PRs, discussions)
- Fast PR review turnaround (target: 48 hours for first review)
- Public recognition of contributors in release notes

### Phase 2: Build Visibility (Months 1-3)

**Content and Talks**
- Publish blog posts about KubeOrch's architecture and design decisions
- Submit talk proposals to KubeCon, Cloud Native Rejekts, and local meetups
- Create demo videos and tutorials
- Write comparison guides (KubeOrch vs Argo Workflows vs Backstage)

**Community Engagement**
- Participate in CNCF TAG App Delivery meetings
- Engage in Kubernetes Slack channels (#sig-apps, #sig-cli)
- Cross-promote with complementary CNCF projects

**Partnership Outreach**
- Identify organizations using Kubernetes workflow tools
- Reach out to DevOps teams at mid-size companies
- Offer to present KubeOrch at company tech talks

### Phase 3: Cultivate Maintainers (Months 3-6)

**Contributor Ladder Progression**
- Actively identify consistent contributors
- Invite regular contributors to become Reviewers (see [CONTRIBUTOR_LADDER.md](https://github.com/KubeOrch/community/blob/main/CONTRIBUTOR_LADDER.md))
- Mentor Reviewers toward Approver and Maintainer roles

**Shared Ownership**
- Assign component ownership to external contributors (e.g., plugin system, specific integrations)
- Invite external contributors to community meetings
- Share decision-making on roadmap priorities

**Formal Mentorship**
- Offer 1:1 onboarding sessions for promising contributors
- Pair external contributors with existing maintainers on features
- Consider participating in CNCF mentoring programs (LFX Mentorship)

## Metrics to Track

| Metric | Target |
|--------|--------|
| External contributors (PRs merged) | 10+ in first 6 months |
| External Reviewers | 2+ within 6 months |
| External Maintainers | 1+ within 6 months |
| Organizations represented | 3+ within 12 months |
| Good first issues available | 5+ at any time |
| PR review turnaround | < 48 hours |

## Risks and Mitigations

| Risk | Mitigation |
|------|-----------|
| Low contributor interest | Increase visibility through talks, blogs, and CNCF TAG engagement |
| Contributors don't progress past one-time PRs | Active mentorship and follow-up after first contribution |
| Competing projects absorb potential contributors | Differentiate clearly and collaborate where possible |
| Burnout of existing maintainers | Distribute work early, automate repetitive tasks |
