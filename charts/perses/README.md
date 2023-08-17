<!-- Any change to the README file must be must be done on README.md.gotmpl file -->

# perses

Perses helm chart

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.37.2](https://img.shields.io/badge/AppVersion-0.37.2-informational?style=flat-square)

## Installing the Chart

To install the chart with the release name `perses`:

```
helm repo add perses https://perses.github.io/perses
helm repo update
helm install perses perses
```

## Values

| Key                                | Type   | Default                             | Description |
|------------------------------------|--------|-------------------------------------|-------------|
| annotations                        | object | `{}`                                |             |
| config.annotations                 | object | `{}`                                |             |
| config.database.file.extension     | string | `"yaml"`                            |             |
| config.database.file.folder        | string | `"/etc/perses/storage"`             |             |
| config.database.sql                | object | `{}`                                |             |
| config.important_dashboards        | list   | `[]`                                |             |
| config.readOnly                    | bool   | `false`                             |             |
| config.schemas.datasources_path    | string | `"/etc/perses/schemas/datasources"` |             |
| config.schemas.panels_path         | string | `"/etc/perses/schemas/panels"`      |             |
| config.schemas.queries_path        | string | `"/etc/perses/schemas/queries"`     |             |
| config.schemas.variables_path      | string | `"/etc/perses/schemas/variables"`   |             |
| fullnameOverride                   | string | `""`                                |             |
| image.name                         | string | `"persesdev/perses"`                |             |
| image.pullPolicy                   | string | `"IfNotPresent"`                    |             |
| image.version                      | string | `""`                                |             |
| ingress.annotations                | object | `{}`                                |             |
| ingress.enabled                    | bool   | `false`                             |             |
| ingress.hostname                   | string | `"perses.local"`                    |             |
| ingress.ingressClassName           | string | `""`                                |             |
| ingress.path                       | string | `"/"`                               |             |
| ingress.pathType                   | string | `"Prefix"`                          |             |
| livenessProbe.enabled              | bool   | `true`                              |             |
| livenessProbe.failureThreshold     | int    | `5`                                 |             |
| livenessProbe.initialDelaySeconds  | int    | `10`                                |             |
| livenessProbe.periodSeconds        | int    | `60`                                |             |
| livenessProbe.successThreshold     | int    | `1`                                 |             |
| livenessProbe.timeoutSeconds       | int    | `5`                                 |             |
| logLevel                           | string | `"info"`                            |             |
| nameOverride                       | string | `""`                                |             |
| persistence.accessModes[0]         | string | `"ReadWriteOnce"`                   |             |
| persistence.annotations            | object | `{}`                                |             |
| persistence.enabled                | bool   | `false`                             |             |
| persistence.labels                 | object | `{}`                                |             |
| persistence.size                   | string | `"8Gi"`                             |             |
| persistence.storageClass           | string | `""`                                |             |
| readinessProbe.enabled             | bool   | `true`                              |             |
| readinessProbe.failureThreshold    | int    | `5`                                 |             |
| readinessProbe.initialDelaySeconds | int    | `5`                                 |             |
| readinessProbe.periodSeconds       | int    | `10`                                |             |
| readinessProbe.successThreshold    | int    | `1`                                 |             |
| readinessProbe.timeoutSeconds      | int    | `5`                                 |             |
| replicas                           | int    | `1`                                 |             |
| resources                          | object | `{}`                                |             |
| service.annotations                | object | `{}`                                |             |
| service.labels                     | object | `{}`                                |             |
| service.port                       | int    | `8080`                              |             |
| service.targetPort                 | int    | `8080`                              |             |
| service.type                       | string | `"ClusterIP"`                       |             |
| serviceAccount.annotations         | object | `{}`                                |             |
| serviceAccount.create              | bool   | `true`                              |             |
| serviceAccount.name                | string | `""`                                |             |

---

Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
