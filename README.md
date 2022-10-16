# Kubernetes Network Policy Demo

This should be a minimal helm chart to debug k8s network policy issues.

## Test

```
helm --dry-run --debug install -f demo/values.yaml demo demo
```
