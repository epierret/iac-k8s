

```markdown
# 🚀 GitLab CI/CD → k3s Lab

Personal lab project demonstrating an end-to-end GitLab CI/CD pipeline deploying applications to a local **k3s Kubernetes cluster** using the **GitLab Kubernetes Agent**.

This repository is intentionally designed as a **living DevOps laboratory**:  
pipelines, configurations, and infrastructure may be **broken, rebuilt, and redesigned** as part of the learning process.

---

## 📊 Architecture Overview

![GitLab CI/CD k3s Architecture](docs/Images/gitlab-k3s-architecture.png)

---

## 📐 Architecture Explanation

The pipeline performs the following steps:

### Code Push
A developer pushes code to the GitLab repository.

### CI Pipeline Triggered
GitLab CI/CD automatically starts the pipeline.

### Build Stage
A container image is built from the application source code.

### Test Stage
Automated tests are executed to validate the build.

### Deployment Stage
The pipeline deploys the application to a local **k3s Kubernetes cluster**.

### Secure Communication
Deployment is handled through the **GitLab Kubernetes Agent (agentk)**.

---

## 🔐 Security Design

This architecture avoids exposing the Kubernetes cluster to the internet.

Key security characteristics:

- No **kubeconfig secrets stored in CI/CD**
- No **inbound network access required**
- Secure **agent-based communication** between GitLab and the cluster

The GitLab Agent maintains a **secure outbound connection** to **GitLab KAS (Kubernetes Agent Server)**, allowing GitLab to interact with the cluster without direct access.

---

## 🧰 Technologies Used

- **GitLab CI/CD**
- **GitLab Kubernetes Agent (agentk)**
- **k3s** (Lightweight Kubernetes)
- **Docker / Container Images**
- **Kubernetes Manifests**

---

## 🎯 Project Goal

This repository serves as an **experimental DevOps playground**.

The objective is to practice and explore:

- Kubernetes deployment workflows  
- GitLab CI/CD pipeline design  
- Secure GitOps-style cluster integration  
- Local Kubernetes environments using k3s  

Because this is a **lab environment**, the repository will continuously evolve:

- configurations may be intentionally **broken**
- pipelines may be **refactored or redesigned**
- infrastructure patterns may **change across branches**

Each branch may explore different topics such as:

- security configurations  
- architecture variations  
- networking approaches  
- service mesh experiments  
- deployment strategies

The goal is not only to build working systems, but also to **understand how to debug, fix, and redesign them**.
```

* ton **lab est présenté comme un laboratoire DevOps évolutif**
* l’idée **break → debug → rebuild** est claire
* ça sonne **plus senior / platform engineering**
* c’est **très bon pour un portfolio**

Si tu veux, je peux aussi te proposer **une version encore plus forte pour recruteurs DevOps (avec sections Observability, GitOps, Security model, Future experiments)**.
