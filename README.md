# kubernetes-ergo

A Kubernetes deployment for the Ergo IRC daemon.

## Overview

This repository contains configuration for deploying Ergo IRC daemon in a Kubernetes environment, with a focus on modern cloud-native technologies and microservices architecture.

## Infrastructure Components

- **Talos**: v1.9.5 - Secure, minimal Linux distribution for Kubernetes
- **Kubernetes**: v1.30.10 - Container orchestration platform
- **OpenEBS**: v4.2.0 - Container attached storage solution
- **ArgoCD**: v2.14.7 - GitOps continuous delivery tool
- **MetalLB**: v0.14.9 - Load balancer implementation for bare metal Kubernetes
- **Istio**: v1.23.5 - Service mesh for microservices
- **Gateway API**: v1.2.1 (experimental) - Modern API for Kubernetes networking

## Architecture

This deployment runs on Talos nodes with Kubernetes 1.30.10, with applications managed through ArgoCD for GitOps-based deployment. Istio is configured in ambient mode and utilizes the experimental Gateway API for network resource management.

Ergo IRC daemon is deployed as a StatefulSet to maintain stable network identities and persistent storage.

## Deployment

All core configuration can be found in the `base/` directory, which contains the standard Kubernetes manifests.

## Getting Started

1. Ensure you have the required infrastructure components installed
2. Apply the base configuration
3. Configure networking and storage according to your environment
