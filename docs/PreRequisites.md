# Pre-requisites for the Solace PubSub+ Deployment

<!-- TOC -->autoauto- [Pre-requisites for the Solace PubSub+ Deployment](#pre-requisites-for-the-solace-pubsub-deployment)auto  - [Perform any necessary platform-specific setup](#perform-any-necessary-platform-specific-setup)auto  - [Deploy Helm package manager](#deploy-helm-package-manager)auto    - [TL;DR;](#tldr)auto    - [Introduction](#introduction)auto    - [Installing Helm v2](#installing-helm-v2)auto    - [Secure Helm and Tiller<a name="securing-helm"></a>](#secure-helm-and-tillera-namesecuring-helma)auto    - [Using Helm](#using-helm)auto    - [Helm upgrade and rollback](#helm-upgrade-and-rollback)auto    - [Helm delete](#helm-delete)auto    - [Using Helm v3](#using-helm-v3)autoauto<!-- /TOC -->

## Perform any necessary platform-specific setup

- GCP
- Amazon EKS
- Azure AKS
- OpenShift
- Minikube

## Deploy Helm package manager

### TL;DR;

This will install and deploy Helm v2.

1. Install the Helm client following [your platform-specific instructions](//helm.sh/docs/using_helm/#installing-the-helm-client ). For Linux, use

```shell
export DESIRED_VERSION=v2.14.3
curl -sSL https://raw.githubusercontent.com/helm/helm/master/scripts/get | bash
```

2. Create a cluster-admin role and init Helm following [the Example: Service account with cluster-admin role](//helm.sh/docs/using_helm/#example-service-account-with-cluster-admin-role )<br/><br/>
**Important:** this will grant Helm's Tiller in-cluster agent `cluster-admin` privileges to enable getting started on most platforms. This should be fine-tuned for Production environments, see section [Secure Helm and Tiller](#securing-helm)


### Introduction
- Helm 2
- Helm 3

### Installing Helm v2
https://helm.sh/docs/using_helm/#installing-helm

### Secure Helm and Tiller<a name="securing-helm"></a>
https://helm.sh/docs/using_helm/#role-based-access-control

### Using Helm
https://helm.sh/docs/using_helm/#using-helm

Helm install command: https://helm.sh/docs/using_helm/#helm-install-installing-a-package
Customizing the Chart Before Installing: https://helm.sh/docs/using_helm/#customizing-the-chart-before-installing

### Helm upgrade and rollback
https://helm.sh/docs/using_helm/#helm-upgrade-and-helm-rollback-upgrading-a-release-and-recovering-on-failure

### Helm delete
https://helm.sh/docs/using_helm/#helm-delete-deleting-a-release

### Using Helm v3