# 🎯 1. Architecture Diagram (for README / Slides)

## 🏗 EKS Architecture

```mermaid
graph TD
    A[User] --> B[kubectl / eksctl]
    B --> C[AWS EKS Control Plane]
    C --> D[Worker Nodes - EC2]
    D --> E[Pods]
    E --> F[Service - LoadBalancer]
    F --> G[Internet]
