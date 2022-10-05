# greeter deployment

This requires that [Helmfile](https://github.com/helmfile/helmfile), [Helm](https://helm.sh/), [Kubectl](https://kubernetes.io/docs/reference/kubectl/), and [Helm-Diff](https://github.com/databus23/helm-diff) plugin be installed.  Obviously, you should have `KUBECONFIG` configured to point to an accessible [Kubernetes](https://kubernetes.io/) cluster.

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
