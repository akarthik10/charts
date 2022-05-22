# mariadb

![Version: 1.0.3](https://img.shields.io/badge/Version-1.0.3-informational?style=flat-square) ![AppVersion: 10.5.16](https://img.shields.io/badge/AppVersion-10.5.16-informational?style=flat-square)

mariadb helm package

**This chart is not maintained by the upstream project and any issues with the chart should be raised [here](https://github.com/k8s-at-home/charts/issues/new/choose)**

## Source Code

* <https://github.com/linuxserver/docker-mariadb>

## Requirements

Kubernetes: `>=1.16.0-0`

## Dependencies

| Repository | Name | Version |
|------------|------|---------|
| https://library-charts.k8s-at-home.com | common | 4.3.0 |

## TL;DR

```console
helm repo add k8s-at-home https://k8s-at-home.com/charts/
helm repo update
helm install mariadb k8s-at-home/mariadb
```

## Installing the Chart

To install the chart with the release name `mariadb`

```console
helm install mariadb k8s-at-home/mariadb
```

## Uninstalling the Chart

To uninstall the `mariadb` deployment

```console
helm uninstall mariadb
```

The command removes all the Kubernetes components associated with the chart **including persistent volumes** and deletes the release.

## Configuration

Read through the [values.yaml](./values.yaml) file. It has several commented out suggested values.
Other values may be used from the [values.yaml](https://github.com/k8s-at-home/library-charts/tree/main/charts/stable/common/values.yaml) from the [common library](https://github.com/k8s-at-home/library-charts/tree/main/charts/stable/common).

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`.

```console
helm install mariadb \
  --set env.TZ="America/New York" \
    k8s-at-home/mariadb
```

Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart.

```console
helm install mariadb k8s-at-home/mariadb -f values.yaml
```

## Custom configuration

N/A

## Values

**Important**: When deploying an application Helm chart you can add more values from our common library chart [here](https://github.com/k8s-at-home/library-charts/tree/main/charts/stable/common)

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env | object | See below | environment variables. See more environment variables in the [mariadb documentation](https://mariadb.org/docs). |
| env.TZ | string | `"UTC"` | Set the container timezone |
| image.pullPolicy | string | `"IfNotPresent"` | image pull policy |
| image.repository | string | `"linuxserver/mariadb"` | image repository |
| image.tag | string | chart.appVersion | image tag |
| ingress.main | object | See values.yaml | Enable and configure ingress settings for the chart under this key. |
| persistence | object | See values.yaml | Configure persistence settings for the chart under this key. |
| probes.liveness.custom | bool | `true` |  |
| probes.liveness.enabled | bool | `true` |  |
| probes.liveness.spec.exec.command[0] | string | `"/usr/bin/env"` |  |
| probes.liveness.spec.exec.command[1] | string | `"bash"` |  |
| probes.liveness.spec.exec.command[2] | string | `"-c"` |  |
| probes.liveness.spec.exec.command[3] | string | `"mysqladmin ping -u root -p$MYSQL_ROOT_PASSWORD"` |  |
| probes.liveness.spec.failureThreshold | int | `3` |  |
| probes.liveness.spec.initialDelaySeconds | int | `10` |  |
| probes.liveness.spec.periodSeconds | int | `10` |  |
| probes.liveness.spec.timeoutSeconds | int | `1` |  |
| probes.readiness.custom | bool | `true` |  |
| probes.readiness.enabled | bool | `true` |  |
| probes.readiness.spec.exec.command[0] | string | `"/usr/bin/env"` |  |
| probes.readiness.spec.exec.command[1] | string | `"bash"` |  |
| probes.readiness.spec.exec.command[2] | string | `"-c"` |  |
| probes.readiness.spec.exec.command[3] | string | `"mysqladmin ping -u root -p$MYSQL_ROOT_PASSWORD"` |  |
| probes.readiness.spec.failureThreshold | int | `3` |  |
| probes.readiness.spec.initialDelaySeconds | int | `10` |  |
| probes.readiness.spec.periodSeconds | int | `10` |  |
| probes.readiness.spec.timeoutSeconds | int | `1` |  |
| probes.startup.custom | bool | `true` |  |
| probes.startup.enabled | bool | `true` |  |
| probes.startup.spec.exec.command[0] | string | `"/usr/bin/env"` |  |
| probes.startup.spec.exec.command[1] | string | `"bash"` |  |
| probes.startup.spec.exec.command[2] | string | `"-c"` |  |
| probes.startup.spec.exec.command[3] | string | `"mysqladmin ping -u root -p$MYSQL_ROOT_PASSWORD"` |  |
| probes.startup.spec.failureThreshold | int | `3` |  |
| probes.startup.spec.initialDelaySeconds | int | `10` |  |
| probes.startup.spec.periodSeconds | int | `10` |  |
| probes.startup.spec.timeoutSeconds | int | `1` |  |
| service | object | See values.yaml | Configures service settings for the chart. |

## Changelog

### Version 1.0.3

#### Added

* Initial version

#### Changed

N/A

#### Fixed

N/A

### Older versions

A historical overview of changes can be found on [ArtifactHUB](https://artifacthub.io/packages/helm/k8s-at-home/mariadb?modal=changelog)

## Support

- See the [Docs](https://docs.k8s-at-home.com/our-helm-charts/getting-started/)
- Open an [issue](https://github.com/k8s-at-home/charts/issues/new/choose)
- Ask a [question](https://github.com/k8s-at-home/organization/discussions)
- Join our [Discord](https://discord.gg/sTMX7Vh) community

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v0.1.1](https://github.com/k8s-at-home/helm-docs/releases/v0.1.1)
