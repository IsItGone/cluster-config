# Cluster Config

A GitOps repository for declarative Kubernetes cluster configuration.

## Overview

This repository stores configuration files that define the desired state of our Kubernetes clusters using GitOps principles. It includes settings for namespaces, infrastructure components, ArgoCD bootstrapping, and application deployments.

## Repository Structure

- **clusters/**: Environment-specific configurations (dev, prod).
- **base/**: Common configurations shared across environments (ArgoCD bootstrapping, shared policies)

## Usage

- The ArgoCD bootstrap script directly installs into the cluster using Helm.
- After installation, ArgoCD's own resources are managed through the GitOps repository.
- ArgoCD automatically synchronizes the configurations with the cluster.

[//]: # (## License)
[//]: # ([Insert license information here])
