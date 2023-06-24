## Network Exporter for Prometheus

### Installation 

```bash
helm install network-exporter . -f values.yaml -n network-exporter --create-namespace
```

### Updating Targets

After updating the probe targets in values.yaml (config.target)

```
1. helm upgrade release
2. kubectl rollout restart daemonset network-exporter -n network-exporter (for the exporter to pickup the new config)
```
