# GitOps Configuration Repository

## Important

This is not the application source code repository.

This repository contains only Kubernetes manifests and Argo CD configurations.
Application source code should live in a separate repository.

## Repository Structure

```bash
.
├── argocd/
│   ├── applications/     # Argo CD Application manifests
│   ├── projects/         # Argo CD AppProject manifests
│   └── appsets/          # Argo CD ApplicationSet manifests
├── base/                 # Base Kubernetes manifests (raw YAML)
├── environments/         # Environment-specific overrides
│   ├── dev/
│   ├── staging/
│   └── production/
└── helm-values/          # Helm values files used by Argo CD
```

## Best Practices Applied

1. Separate repos: app code and configs are separated.
2. Directory-based environments: no permanent branches for environments.
3. Clear manifest separation: Argo CD resources vs Kubernetes resources.
4. GitOps: everything declarative and in Git.
