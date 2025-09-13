# Contributing to KubeOrch

Welcome to KubeOrch! We're excited that you're interested in contributing to our visual Kubernetes workflow orchestrator. This guide will help you get started with contributing to the project.

## Our Mission

KubeOrch aims to provide a drag-and-drop deployment platform for Kubernetes, making container orchestration accessible to developers of all skill levels while providing cost optimization and alerting features for companies using their own infrastructure.

## How to Contribute

### Our Workflow

Contributing to KubeOrch should be as simple as possible. Have a question? Want to discuss something? Want to contribute something? Just open an Issue or a Pull Request.

If you spot a bug or want to change something straightforward, go ahead and open an Issue and/or a Pull Request with your changes.

For larger changes that require more planning and discussion, we encourage opening an Issue first to discuss the proposed changes. Examples of these types of changes include:
- New UI components or workflows
- Architectural changes to the drag-and-drop interface
- Backend API modifications
- New cloud provider integrations
- Changes to the deployment pipeline

### Getting Started

To make yourself comfortable with the codebase, look for Issues marked with labels like `good-first-issue`, `help-wanted`, or `bug`. Any help is highly appreciated.

Our project consists of three main components:
1. **Frontend**: Drag-and-drop UI for creating Kubernetes configurations
2. **Backend**: API server handling deployments and integrations
3. **Integration Layer**: Kubernetes cluster management and deployment orchestration

### Development Approach

We follow a feature-based development approach rather than component-based to minimize integration challenges. Our initial focus areas include:
- Visual workflow builder with real-time YAML preview
- GitHub integration for automated deployment triggers
- AWS EKS deployment support (with plans for multi-cloud expansion)
- Cost optimization and alerting capabilities

## Technical Guidelines

### Architecture Overview

KubeOrch is designed as a self-deployable application to mitigate security risks and reduce infrastructure costs. The platform includes:
- Docker Compose packaging for easy deployment
- Self-hosted database for user configurations and deployment states
- IAM roles integration for secure cloud access
- Nix Packs tool integration for automatic containerization

### Testing

Untested features do not exist. When contributing, please ensure:
- Unit tests cover your code changes
- Integration tests validate end-to-end workflows
- UI changes include appropriate testing for drag-and-drop functionality
- All tests can be run locally without CI dependency

### Code Quality Standards

- Follow Go best practices for backend development
- Use modern React patterns for frontend development
- Implement proper error handling and logging
- Ensure responsive design for the drag-and-drop interface
- Write clear, self-documenting code

## Pull Request Process

### Before You Submit

1. **Open an Issue** for discussion if your change is significant
2. **Test your changes** thoroughly, including edge cases
3. **Follow our coding standards** and architectural patterns
4. **Update documentation** if your changes affect user workflows

### Pull Request Guidelines

- Create descriptive commit messages
- Keep Pull Requests focused on a single feature or fix
- Include tests for new functionality
- Update relevant documentation
- Be responsive to feedback during code review

### Draft Pull Requests

Consider opening your Pull Request as a draft if:
- You want to initiate early discussion
- The changes are not complete
- You're exploring a new feature direction

Draft PRs help save CI resources and signal to reviewers that the code isn't ready for final review.

### Automated Testing

Automated testing will be triggered on Pull Requests from organization members. New contributors may need approval before automated tests run.

## Developer Certificate of Origin (DCO)

We require every contributor to certify that they are legally permitted to contribute to our project. Please sign your commits by adding `--signoff` to your git command line.

Your commit message should contain:
```
Signed-off-by: Your Name <your.email@example.com>
```

## Getting Help

### Code Reviews

Maintainers will review your code and provide productive feedback. If you feel blocked or your Pull Request needs attention:
- Comment on your Issue or Pull Request
- Reach out to maintainers directly
- Join our community discussions

### Becoming a Member

Contributors who frequently contribute to the project may ask to join the KubeOrch organization. Active contributors who demonstrate:
- Consistent, quality contributions
- Understanding of project goals and architecture  
- Collaborative approach to development
- Commitment to our Code of Conduct

are welcome to apply for membership.

## Development Environment Setup

### Prerequisites
- Go 1.21+ (for backend development)
- Node.js 18+ (for frontend development)
- Docker and Docker Compose
- Kubernetes cluster access (minikube/kind for local development)
- Git

### Local Development
Our self-deployable architecture means you can run the entire stack locally using Docker Compose, including:
- Frontend application
- Backend API server
- Database
- Local Kubernetes integration

## Project Phases

### Current Phase: Foundation & MVP
- Focus on frontend and backend development
- Basic YAML generation capabilities
- Drag-and-drop configuration interface
- Direct deployment to Kubernetes clusters

### Upcoming Features
- GitHub integration for automated deployments
- Multi-cloud provider support (starting with AWS EKS)
- Advanced cost optimization algorithms
- Enhanced security and compliance features

## Community

We are building KubeOrch to be a community-driven project that makes Kubernetes accessible to everyone. Whether you're interested in:
- Frontend development (React, TypeScript, drag-and-drop interfaces)
- Backend development (Go, Kubernetes APIs, cloud integrations)
- DevOps and infrastructure (Kubernetes, CI/CD, deployment automation)
- Documentation and user experience
- Community building and advocacy

Your contributions are welcome and valued!

---

Thank you for contributing to KubeOrch! Together, we're making Kubernetes deployment beautiful and accessible.