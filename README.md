# glueops-network-exporter

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.7.2](https://img.shields.io/badge/AppVersion-1.7.2-informational?style=flat-square)

Prometheus exporter for monitoring ICMP,MTR,TCP,HTTP probes from all nodes in the cluster

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| args | list | `[]` |  |
| config.conf.nameserver_timeout | string | `"250ms"` |  |
| config.conf.refresh | string | `"2m"` |  |
| config.http_get.interval | string | `"15m"` |  |
| config.http_get.timeout | string | `"5s"` |  |
| config.icmp.count | int | `6` |  |
| config.icmp.interval | string | `"3s"` |  |
| config.icmp.timeout | string | `"1s"` |  |
| config.mtr.count | int | `6` |  |
| config.mtr.interval | string | `"3s"` |  |
| config.mtr.max-hops | int | `30` |  |
| config.mtr.timeout | string | `"500ms"` |  |
| config.targets[0].host | string | `"8.8.8.8"` |  |
| config.targets[0].name | string | `"google-dns"` |  |
| config.targets[0].type | string | `"ICMP+MTR"` |  |
| config.targets[1].host | string | `"1.1.1.1"` |  |
| config.targets[1].name | string | `"cloudflare-dns"` |  |
| config.targets[1].type | string | `"ICMP+MTR"` |  |
| config.targets[2].host | string | `"glueops-network-exporter.glueops-core-network-exporter.svc.cluster.local"` |  |
| config.targets[2].name | string | `"glueops-network-exporter"` |  |
| config.targets[2].type | string | `"ICMP+MTR"` |  |
| config.targets[3].host | string | `"http://public-ingress-nginx-controller.glueops-core-public-ingress-nginx.svc.cluster.local"` |  |
| config.targets[3].name | string | `"nginx"` |  |
| config.targets[3].type | string | `"HTTPGet"` |  |
| config.targets[4].host | string | `"public-ingress-nginx-controller.glueops-core-public-ingress-nginx.svc.cluster.local:80"` |  |
| config.targets[4].name | string | `"nginx"` |  |
| config.targets[4].type | string | `"TCP"` |  |
| config.tcp.interval | string | `"3s"` |  |
| config.tcp.timeout | string | `"1s"` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"syepes/network_exporter"` |  |
| image.tag | string | `"1.7.2"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| resources | object | `{}` |  |
| securityContext.capabilities.add[0] | string | `"CAP_NET_RAW"` |  |
| securityContext.capabilities.add[1] | string | `"CAP_NET_ADMIN"` |  |
| securityContext.privileged | bool | `true` |  |
| service.annotations."prometheus.io/port" | string | `"9427"` |  |
| service.annotations."prometheus.io/scrape" | string | `"true"` |  |
| service.port | int | `9427` |  |
| service.type | string | `"ClusterIP"` |  |
| tolerations | list | `[]` |  |
