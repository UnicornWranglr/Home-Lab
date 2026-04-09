# Home Lab

A personal infrastructure lab built to develop DevOps and platform engineering skills.

## Overview

3-node K3s Kubernetes cluster running on Ubuntu Server 24.04, provisioned and 
managed entirely with Ansible from a dedicated management node.

## Infrastructure

| Host | Role |
|------|------|
| PK-MGMT-001 | Management node — Ansible, Prometheus, Grafana |
| LAB-K8S-001 | K3s control plane |
| LAB-K8S-002 | K3s worker node |
| LAB-K8S-003 | K3s worker node |

## Stack

- **Provisioning:** Ansible
- **Orchestration:** K3s (Kubernetes)
- **Monitoring:** Prometheus + Grafana + Node Exporter
- **Version Control:** Git + GitHub

## Playbooks

| Playbook | Purpose |
|----------|---------|
| `install-k3s.yml` | Provisions K3s cluster across all nodes |
| `deploy-node-exporter.yml` | Deploys Prometheus Node Exporter |
| `patch-linux.yml` | Patch management across all Linux hosts |
| `check-uptime.yml` | Uptime checks across infrastructure |

## Roadmap

- [ ] Migrate cluster to RHEL 9
- [ ] Deploy application workloads to cluster
- [ ] Set up GitOps with ArgoCD
- [ ] CI/CD pipelines with GitHub Actions
- [ ] Cloudflare Tunnel for external access
