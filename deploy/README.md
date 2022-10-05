# greeter deployment

This requires that [Helmfile](https://github.com/helmfile/helmfile), [Helm](https://helm.sh/), [Kubectl](https://kubernetes.io/docs/reference/kubectl/), and [Helm-Diff](https://github.com/databus23/helm-diff) plugin be installed.  Obviously, you should have `KUBECONFIG` configured to point to an accessible [Kubernetes](https://kubernetes.io/) cluster.

## Prerequisite

The image should be published somewhere accessible.  I have published a version in my personal repository, but it would be more optimal to publish the image to Docker Hub or private registry like ]ACR](https://azure.microsoft.com/free/container-registry/), [GAR](https://cloud.google.com/artifact-registry), [GCR](https://cloud.google.com/container-registry), [ECR](https://aws.amazon.com/ecr/), [GHCR](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry), [Harbor](https://goharbor.io/), [Quay](https://quay.io/), [Distribution](https://github.com/distribution/distribution), [JCR](https://jfrog.com/container-registry/), [GLCR](https://docs.gitlab.com/ee/user/packages/container_registry/), etc.

```bash
export DOCKER_REGISTRY="darknerd"
```

## General instructions

```bash
helmfile apply
```

## Instructions for service meshes

### Consul Connect service mesh

```bash
export CCSM_ENABLED="true"
helmfile apply
```
