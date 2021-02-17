# teslamate

![Version: 3.5.1](https://img.shields.io/badge/Version-3.5.1-informational?style=flat-square) ![AppVersion: v1.20.0](https://img.shields.io/badge/AppVersion-v1.20.0-informational?style=flat-square)

A self-hosted data logger for your Tesla 🚘

**Homepage:** <https://github.com/k8s-at-home/charts/tree/master/charts/teslamate>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| billimek | jeff@billimek.com |  |

## Source Code

* <https://github.com/adriankumpf/teslamate>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | postgresql | 10.2.7 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| checkOrigin | bool | `false` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"teslamate/teslamate"` |  |
| image.tag | string | `"1.20.0"` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0] | string | `"chart-example.local"` |  |
| ingress.path | string | `"/"` |  |
| ingress.tls | list | `[]` |  |
| locale | string | `"en"` |  |
| mqtt.enabled | bool | `false` |  |
| mqtt.host | string | `nil` |  |
| mqtt.password | string | `nil` |  |
| mqtt.tls | string | `nil` |  |
| mqtt.tlsAcceptInvalid | string | `nil` |  |
| mqtt.username | string | `nil` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| postgresql.enabled | bool | `true` |  |
| postgresql.image.repository | string | `"postgres"` |  |
| postgresql.image.tag | float | `12.1` |  |
| postgresql.persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| postgresql.persistence.enabled | bool | `true` |  |
| postgresql.persistence.mountPath | string | `"/data/"` |  |
| postgresql.persistence.size | string | `"8Gi"` |  |
| postgresql.persistence.storageClass | string | `nil` |  |
| postgresql.postgresqlDataDir | string | `"/data/pgdata"` |  |
| postgresql.postgresqlDatabase | string | `"teslamate"` |  |
| postgresql.postgresqlPassword | string | `"teslamate"` |  |
| postgresql.postgresqlUsername | string | `"teslamate"` |  |
| probes.liveness.failureThreshold | int | `15` |  |
| probes.liveness.periodSeconds | int | `10` |  |
| probes.readiness.failureThreshold | int | `15` |  |
| probes.readiness.periodSeconds | int | `10` |  |
| probes.startup.failureThreshold | int | `30` |  |
| probes.startup.initialDelaySeconds | int | `15` |  |
| probes.startup.periodSeconds | int | `10` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| service.port | int | `4000` |  |
| service.type | string | `"ClusterIP"` |  |
| timeZone | string | `"UTC"` |  |
| tolerations | list | `[]` |  |
| virtualHost | string | `nil` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)