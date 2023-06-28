## Network Exporter for Prometheus

### Installation 

```bash
helm install glueops-network-exporter . -f values.yaml -n glueops-core-network-exporter --create-namespace
```

### Updating Targets

After updating the probe targets in values.yaml (config.target)

```
1. helm upgrade release
2. kubectl rollout restart daemonset glueops-network-exporter  -n glueops-core-network-exporter (for the exporter to pickup the new config)
```
