# Cloud Native Landscape Submission Guide

Instructions for listing KubeOrch on the [CNCF Cloud Native Landscape](https://landscape.cncf.io/).

## Prerequisites

- [ ] Project logo in SVG format (must be square, preferably without text)
- [ ] Public GitHub repository
- [ ] Apache 2.0 license

## Submission Steps

### 1. Fork the Landscape Repository

Fork https://github.com/cncf/landscape

### 2. Add the Project Entry

Edit `landscape.yml` and add KubeOrch under the appropriate category.

**Recommended category**: `App Definition and Development` > `Application Definition & Image Build`

**Alternative category**: `Orchestration & Management` > `Scheduling & Orchestration`

Add the following entry:

```yaml
- item:
    name: KubeOrch
    homepage_url: https://docs.kubeorch.dev
    repo_url: https://github.com/KubeOrch/core
    logo: kubeorch.svg
    description: Visual Kubernetes workflow orchestrator that transforms complex YAML configurations into intuitive drag-and-drop interfaces.
    project: null
    additional_repos:
      - repo_url: https://github.com/KubeOrch/ui
      - repo_url: https://github.com/KubeOrch/cli
```

### 3. Add the Logo

Place the SVG logo in the `hosted_logos/` directory as `kubeorch.svg`.

**Logo requirements:**
- SVG format
- Square aspect ratio
- No text in the logo (text will be added by the landscape)
- Clean, simple design that works at small sizes

### 4. Submit the Pull Request

Create a PR to the `cncf/landscape` repository with:
- The `landscape.yml` change
- The logo file

**PR title**: `Add KubeOrch to App Definition and Development`

**PR description**:
```
Adding KubeOrch, a visual Kubernetes workflow orchestrator.

- Website: https://docs.kubeorch.dev
- GitHub: https://github.com/KubeOrch
- License: Apache 2.0
- Description: KubeOrch transforms complex Kubernetes YAML configurations into
  intuitive drag-and-drop interfaces, providing end-to-end integration from source
  code to production deployment.
```

### 5. After Acceptance

Once the landscape PR is merged:

1. Update the CNCF sandbox application to note landscape listing
2. Add the landscape badge to READMEs if desired

## Also Register on LFX Insights

1. Go to https://insights.lfx.linuxfoundation.org/
2. Submit the project for tracking
3. This provides contributor analytics that CNCF reviewers may check
