# JuiceFS Cache Group Operator Helm Chart


![Version: 0.3.1](https://img.shields.io/badge/Version-0.3.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.3.1](https://img.shields.io/badge/AppVersion-0.3.1-informational?style=flat-square)

This Helm chart installs the JuiceFS Cache Group Operator.

**Homepage:** <https://github.com/juicedata/juicefs-cache-group-operator>

## Maintainers

| Name           | Email               | Url                   |
| -------------- | ------------------- | --------------------- |
| Juicedata Inc. | <team@juicedata.io> | <https://juicefs.com> |

## Source Code

* <https://github.com/juicedata/juicefs-cache-group-operator>

## Requirements

Kubernetes: `>=1.14.0-0`

## Values

The following table lists the configurable parameters of the JuiceFS Cache Group Operator chart and their default values.

| Parameter                            | Description                                           | Default                                                              |
| ------------------------------------ | ----------------------------------------------------- | -------------------------------------------------------------------- |
| `replicaCount`                       | Number of replicas for the deployment                 | `2`                                                                  |
| `image.repository`                   | Image repository                                      | `juicedata/juicefs-cache-group-operator`                             |
| `image.pullPolicy`                   | Image pull policy                                     | `IfNotPresent`                                                       |
| `image.tag`                          | Image tag                                             | `${Chart.AppVersion}`                                                |
| `logLevel`                           | Logging verbosity level                               | `info`                                                               |
| `logEncoder`                         | Log encoding format                                   | `console`                                                            |
| `imagePullSecrets`                   | Secrets for image pull                                |                                                                      |
| `nameOverride`                       | Override the name of the chart                        |                                                                      |
| `fullnameOverride`                   | Override the full name of the chart                   |                                                                      |
| `serviceAccount.create`              | Specifies whether a service account should be created | `true`                                                               |
| `serviceAccount.annotations`         | Annotations to add to the service account             |                                                                      |
| `serviceAccount.name`                | The name of the service account to use                |                                                                      |
| `leaderElection.enabled`             | Enable leader election for controller manager         | `true`                                                               |
| `podAnnotations`                     | Annotations to add to the pod                         |                                                                      |
| `podLabels`                          | Labels to add to the pod                              |                                                                      |
| `podSecurityContext`                 | Security context for the pod                          | `{ runAsNonRoot: true }`                                             |
| `securityContext`                    | Security context for the container                    | `{ allowPrivilegeEscalation: false, capabilities: { drop: [ALL] } }` |
| `resources.limits.cpu`               | CPU resource limits                                   | `500m`                                                               |
| `resources.limits.memory`            | Memory resource limits                                | `128Mi`                                                              |
| `resources.requests.cpu`             | CPU resource requests                                 | `10m`                                                                |
| `resources.requests.memory`          | Memory resource requests                              | `64Mi`                                                               |
| `livenessProbe.httpGet.path`         | Path for the liveness probe                           | `/healthz`                                                           |
| `livenessProbe.httpGet.port`         | Port for the liveness probe                           | `8081`                                                               |
| `livenessProbe.initialDelaySeconds`  | Initial delay for the liveness probe                  | `15`                                                                 |
| `livenessProbe.periodSeconds`        | Period for the liveness probe                         | `20`                                                                 |
| `readinessProbe.httpGet.path`        | Path for the readiness probe                          | `/readyz`                                                            |
| `readinessProbe.httpGet.port`        | Port for the readiness probe                          | `8081`                                                               |
| `readinessProbe.initialDelaySeconds` | Initial delay for the readiness probe                 | `5`                                                                  |
| `readinessProbe.periodSeconds`       | Period for the readiness probe                        | `10`                                                                 |
| `nodeSelector`                       | Node selector for pod assignment                      |                                                                      |
| `tolerations`                        | Tolerations for pod assignment                        |                                                                      |
| `affinity`                           | Affinity settings for pod assignment                  |                                                                      |
