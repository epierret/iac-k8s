🚀 GitLab CI/CD → k3s Lab

Personal lab project demonstrating an end-to-end GitLab CI/CD pipeline deploying applications to a local k3s Kubernetes cluster using the GitLab Kubernetes Agent.



📊 Architecture Overview

This diagram illustrates the full deployment workflow:

Developer
   │
   ▼
GitLab Repository
   │
   ▼
GitLab CI/CD Pipeline
   │
   ▼
GitLab Kubernetes Agent (agentk)
   │
   ▼
Local k3s Kubernetes Cluster

https://gitlab.com/pierretenrique/kubernetes-test/-/blob/29e36449d99b9e8d6e32c0762fd98b48731ebc0c/Docs/Images/gitlab-k3s-architecture.png


📐 Architecture Explanation

The pipeline performs the following steps:

Code Push

A developer pushes code to the GitLab repository.

CI Pipeline Triggered

GitLab CI/CD automatically starts the pipeline.

Build Stage

A container image is built from the application source code.

Test Stage

Automated tests are executed to validate the build.


🔐 Security Design

This architecture avoids exposing the Kubernetes cluster to the internet.

Key security benefits:

No kubeconfig secrets stored in CI/CD

No inbound network access required

Secure agent-based communication between GitLab and the cluster

The GitLab agent connects outbound to GitLab KAS, enabling GitLab to manage the cluster securely.
Deployment Stage

The pipeline deploys the application to a local k3s Kubernetes cluster.

Secure Communication

Deployment is handled through the GitLab Kubernetes Agent (agentk).



🧰 Technologies Used

GitLab CI/CD

GitLab Kubernetes Agent (agentk)

k3s (Lightweight Kubernetes)

Docker / Container Images

Kubernetes Manifests


🎯 Project Goal

This lab was created to practice and demonstration purpose and also vocation to be broken and rebuilt.

each branch will have different security , architecture , service mesh purpose 

Kubernetes deployment workflows

GitLab CI/CD pipeline design

Secure GitOps-style cluster integration

Local Kubernetes environments using k3s

The agent maintains a secure outbound connection to GitLab KAS (Kubernetes Agent Server).

