# 🚀 GitLab CI/CD → k3s Lab

> Personal lab for practicing end-to-end GitLab pipelines deployed to a local k3s cluster using the GitLab Kubernetes Agent.

---

## 📊 Architecture Overview

![GitLab CI/CD k3s Architecture](docs/images/gitlab-k3s-architecture.png)

This diagram shows the full deployment flow:

Developer → GitLab Repository → CI/CD Pipeline → GitLab Kubernetes Agent → Local k3s Cluster.

---

## 📐 Architecture

---

### 3. Optional (very good for DevOps portfolios)

Add a **short explanation under the image**:

```markdown
The pipeline builds a container image, runs tests, and deploys to a local
k3s Kubernetes cluster using the GitLab Kubernetes Agent (agentk).
The agent maintains a secure outbound connection to GitLab KAS,
allowing deployments without exposing the cluster or storing kubeconfig
secrets in CI.on