# cert-manager-webhook-safedns

## Introduction

This Helm chart installs the SafeDNS cert-manager webhook into a Kubernetes cluster

## Prerequisites

* Kubernetes 1.17+ (see note [here](https://github.com/ukfast/cert-manager-webhook-safedns#installing))

## Installation

* `helm repo add ukfast https://ukfast.github.io/helm-charts`
* `helm repo update`
* `helm install cert-manager-webhook-safedns ukfast/cert-manager-webhook-safedns`

## Configuration

| Parameter | Description | Default |
| --------- | ----------- | ------- |
| `groupName`                       | Name of API group                 | `acme.k8s.ukfast.io` |
| **Image** |
| `image.repository`                | Image                             | `ukfast/cert-manager-webhook-safedns` |
| `image.tag`                       | Image tag                         | `latest` |
| **Cert Manager** |
| `certManager.namespace`           | cert-manager namespace            | `cert-manager` |
| `certManager.serviceAccountName`  | cert-manager service account name | `cert-manager` |
| **Resources** |
| `resources`                       | CPU/Memory resources              | `{}` |
| **Service** |
| `service.type`                    | Service type                      | `NodePort` |
| `service.port`                    | Service port                      | `80` |
| **Node Selector** |
| `nodeSelector`                    | Node selector                     | `{}` |
| **Tolerations** |
| `tolerations`                     | Tolerations                       | `[]` |
| **Affinity** |
| `affinity`                        | Affinity                          | `{}` |