# Kubernetes Network Policy Demo

This should be a minimal helm chart to debug k8s network policy issues.

## Test

```
helm --dry-run --debug install -f demo/values.yaml demo demo
```

## Setting up IP Address Outbound

For google we use (for now) their entire ASN... if you have it in a file you can go:

```
while read line; do echo "- ipBlock:
    cidr: $line"; done < gasn >> dump.txt
```

Which spits out the ip-block stuff you need for the network policy.