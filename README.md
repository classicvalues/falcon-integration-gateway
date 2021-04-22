# falcon-integration-gateway [![Python Lint](https://github.com/CrowdStrike/falcon-integration-gateway/actions/workflows/linting.yml/badge.svg)](https://github.com/CrowdStrike/falcon-integration-gateway/actions/workflows/linting.yml) [![Container Build on Quay](https://quay.io/repository/crowdstrike/falcon-integration-gateway/status "Docker Repository on Quay")](https://quay.io/repository/crowdstrike/falcon-integration-gateway)

Falcon Integration Gateway (FIG) forwards threat detection findings from CrowdStrike Falcon platform to the [backend](fig/backends) of your choice.

Detection findings generated by CrowdStrike Falcon platform inform you about suspicious files and behaviors in your environment. You will see detections on a range of activities from the presence of a bad file (indicator of compromise (IOC)) to a nuanced collection of suspicious behaviors (indicator of attack (IOA)) occurring on one of your hosts or containers. You can learn more about the individual detections in [Falcon documentation](https://falcon.crowdstrike.com/support/documentation/40/mitre-based-falcon-detections-framework).

This project facilitates the export of the individual detections from CrowdStrike Falcon to third-party security dashboards (so called backends). The export is useful in cases where security operation team workflows are tied to given third-party solution to get early real-time heads-up about malicious activities detected by CrowdStrike Falcon platform.

Currently available backends are
 * [AWS backend](fig/backends/aws) - pushes events to AWS Security Hub
 * [Azure backend](fig/backends/azure) - pushes events to Azure Log Analytics
 * [GCP backend](fig/backends/gcp) - pushes events to GCP Security Command Center
 * [Workspace ONE backend](fig/backends/workspaceone) - pushes events to VMware Workspace ONE Intelligence
 * [Chronicle backend](fig/backends/chronicle) - pushed events to Chronicle Backstory

Falcon Integration Gateway (FIG) is an open source project, not CrowdStrike product. As such it carries no formal support, expressed or implied.

## Deployment Guide

- [Deployment to AKS](docs/aks)
- [Deployment to GKE](docs/gke)

## Developer Guide

Start with learning about the different [backends](fig/backends). Instructions may differ slightly depending on the backend of interest.
