# juicefs-csi-driver

![Version: 0.19.6](https://img.shields.io/badge/Version-0.19.6-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.23.3](https://img.shields.io/badge/AppVersion-0.23.3-informational?style=flat-square)

A Helm chart for JuiceFS CSI Driver

**Homepage:** <https://github.com/juicedata/juicefs-csi-driver>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Juicedata Inc. | <team@juicedata.io> | <https://juicefs.com> |

## Source Code

* <https://github.com/juicedata/juicefs-csi-driver>

## Requirements

Kubernetes: `>=1.14.0-0`

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| controller.affinity | object | `{}` |  |
| controller.cacheClientConf | bool | `true` |  |
| controller.enabled | bool | `true` |  |
| controller.envs | string | `nil` | Extra envs of CSI Controller Example:  - name: ENABLE_APISERVER_LIST_CACHE    value: "true" |
| controller.leaderElection.enabled | bool | `true` |  |
| controller.leaderElection.leaderElectionNamespace | string | `""` |  |
| controller.leaderElection.leaseDuration | string | `""` |  |
| controller.nodeSelector | object | `{}` |  |
| controller.priorityClassName | string | `"system-cluster-critical"` |  |
| controller.provisioner | bool | `false` |  |
| controller.replicas | int | `2` |  |
| controller.resources.limits.cpu | string | `"1000m"` |  |
| controller.resources.limits.memory | string | `"1Gi"` |  |
| controller.resources.requests.cpu | string | `"100m"` |  |
| controller.resources.requests.memory | string | `"512Mi"` |  |
| controller.service.port | int | `9909` |  |
| controller.service.type | string | `"ClusterIP"` |  |
| controller.terminationGracePeriodSeconds | int | `30` |  |
| controller.tolerations[0].key | string | `"CriticalAddonsOnly"` |  |
| controller.tolerations[0].operator | string | `"Exists"` |  |
| dashboard.affinity | object | `{}` |  |
| dashboard.enabled | bool | `true` |  |
| dashboard.envs | list | `[]` |  |
| dashboard.hostNetwork | bool | `false` |  |
| dashboard.ingress.annotations | object | `{}` |  |
| dashboard.ingress.className | string | `"nginx"` |  |
| dashboard.ingress.enabled | bool | `false` |  |
| dashboard.ingress.hosts[0].host | string | `""` |  |
| dashboard.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| dashboard.ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| dashboard.ingress.tls | list | `[]` |  |
| dashboard.leaderElection.enabled | bool | `false` |  |
| dashboard.leaderElection.leaderElectionNamespace | string | `""` |  |
| dashboard.leaderElection.leaseDuration | string | `""` |  |
| dashboard.nodeSelector | object | `{}` |  |
| dashboard.priorityClassName | string | `"system-node-critical"` |  |
| dashboard.replicas | int | `1` |  |
| dashboard.resources.limits.cpu | string | `"1000m"` |  |
| dashboard.resources.limits.memory | string | `"1Gi"` |  |
| dashboard.resources.requests.cpu | string | `"100m"` |  |
| dashboard.resources.requests.memory | string | `"200Mi"` |  |
| dashboard.service.port | int | `8088` |  |
| dashboard.service.type | string | `"ClusterIP"` |  |
| dashboard.tolerations[0].key | string | `"CriticalAddonsOnly"` |  |
| dashboard.tolerations[0].operator | string | `"Exists"` |  |
| dashboardImage.pullPolicy | string | `""` |  |
| dashboardImage.repository | string | `"juicedata/csi-dashboard"` |  |
| dashboardImage.tag | string | `"v0.23.3"` |  |
| defaultMountImage.ce | string | `""` |  |
| defaultMountImage.ee | string | `""` |  |
| dnsConfig | object | `{}` |  |
| dnsPolicy | string | `"ClusterFirstWithHostNet"` |  |
| hostAliases | list | `[]` |  |
| image.pullPolicy | string | `""` |  |
| image.repository | string | `"juicedata/juicefs-csi-driver"` |  |
| image.tag | string | `"v0.23.3"` |  |
| imagePullSecrets | list | `[]` |  |
| immutable | bool | `false` |  |
| jfsConfigDir | string | `"/var/lib/juicefs/config"` |  |
| jfsMountDir | string | `"/var/lib/juicefs/volume"` |  |
| kubeletDir | string | `"/var/lib/kubelet"` |  |
| mountMode | string | `"mountpod"` |  |
| node.affinity | object | `{}` |  |
| node.enabled | bool | `true` |  |
| node.envs | list | `[]` | Extra envs of CSI Node Example:  - name: ENABLE_APISERVER_LIST_CACHE    value: "true" |
| node.hostNetwork | bool | `false` |  |
| node.ifPollingKubelet | bool | `true` |  |
| node.mountPodNonPreempting | bool | `false` |  |
| node.nodeSelector | object | `{}` |  |
| node.priorityClassName | string | `"system-node-critical"` |  |
| node.resources.limits.cpu | string | `"1000m"` |  |
| node.resources.limits.memory | string | `"1Gi"` |  |
| node.resources.requests.cpu | string | `"100m"` |  |
| node.resources.requests.memory | string | `"512Mi"` |  |
| node.storageClassShareMount | bool | `false` |  |
| node.terminationGracePeriodSeconds | int | `30` |  |
| node.tolerations[0].key | string | `"CriticalAddonsOnly"` |  |
| node.tolerations[0].operator | string | `"Exists"` |  |
| node.updateStrategy.rollingUpdate.maxUnavailable | string | `"50%"` |  |
| serviceAccount.controller.annotations | object | `{}` |  |
| serviceAccount.controller.create | bool | `true` |  |
| serviceAccount.controller.name | string | `"juicefs-csi-controller-sa"` |  |
| serviceAccount.dashboard.annotations | object | `{}` |  |
| serviceAccount.dashboard.create | bool | `true` |  |
| serviceAccount.dashboard.name | string | `"juicefs-csi-dashboard-sa"` |  |
| serviceAccount.node.annotations | object | `{}` |  |
| serviceAccount.node.create | bool | `true` |  |
| serviceAccount.node.name | string | `"juicefs-csi-node-sa"` |  |
| sidecars.csiProvisioner.image.pullPolicy | string | `""` |  |
| sidecars.csiProvisioner.image.repository | string | `"quay.io/k8scsi/csi-provisioner"` |  |
| sidecars.csiProvisioner.image.tag | string | `"v1.6.0"` |  |
| sidecars.csiProvisioner.resources.limits.cpu | string | `"100m"` |  |
| sidecars.csiProvisioner.resources.limits.memory | string | `"200Mi"` |  |
| sidecars.csiProvisioner.resources.requests.cpu | string | `"10m"` |  |
| sidecars.csiProvisioner.resources.requests.memory | string | `"100Mi"` |  |
| sidecars.csiResizer.image.pullPolicy | string | `""` |  |
| sidecars.csiResizer.image.repository | string | `"quay.io/k8scsi/csi-resizer"` |  |
| sidecars.csiResizer.image.tag | string | `"v1.0.1"` |  |
| sidecars.csiResizer.resources.limits.cpu | string | `"100m"` |  |
| sidecars.csiResizer.resources.limits.memory | string | `"200Mi"` |  |
| sidecars.csiResizer.resources.requests.cpu | string | `"10m"` |  |
| sidecars.csiResizer.resources.requests.memory | string | `"100Mi"` |  |
| sidecars.livenessProbe.image.pullPolicy | string | `""` |  |
| sidecars.livenessProbe.image.repository | string | `"quay.io/k8scsi/livenessprobe"` |  |
| sidecars.livenessProbe.image.tag | string | `"v1.1.0"` |  |
| sidecars.livenessProbe.resources.limits.cpu | string | `"100m"` |  |
| sidecars.livenessProbe.resources.limits.memory | string | `"200Mi"` |  |
| sidecars.livenessProbe.resources.requests.cpu | string | `"10m"` |  |
| sidecars.livenessProbe.resources.requests.memory | string | `"100Mi"` |  |
| sidecars.nodeDriverRegistrar.image.pullPolicy | string | `""` |  |
| sidecars.nodeDriverRegistrar.image.repository | string | `"quay.io/k8scsi/csi-node-driver-registrar"` |  |
| sidecars.nodeDriverRegistrar.image.tag | string | `"v2.1.0"` |  |
| sidecars.nodeDriverRegistrar.resources.limits.cpu | string | `"100m"` |  |
| sidecars.nodeDriverRegistrar.resources.limits.memory | string | `"200Mi"` |  |
| sidecars.nodeDriverRegistrar.resources.requests.cpu | string | `"10m"` |  |
| sidecars.nodeDriverRegistrar.resources.requests.memory | string | `"100Mi"` |  |
| storageClasses[0].allowVolumeExpansion | bool | `true` |  |
| storageClasses[0].backend.accessKey | string | `""` |  |
| storageClasses[0].backend.bucket | string | `""` |  |
| storageClasses[0].backend.configs | string | `""` |  |
| storageClasses[0].backend.envs | string | `""` |  |
| storageClasses[0].backend.formatOptions | string | `""` |  |
| storageClasses[0].backend.metaurl | string | `""` |  |
| storageClasses[0].backend.name | string | `""` |  |
| storageClasses[0].backend.secretKey | string | `""` |  |
| storageClasses[0].backend.storage | string | `""` |  |
| storageClasses[0].backend.token | string | `""` |  |
| storageClasses[0].backend.trashDays | string | `""` |  |
| storageClasses[0].cachePVC | string | `""` |  |
| storageClasses[0].enabled | bool | `false` |  |
| storageClasses[0].mountOptions | string | `nil` |  |
| storageClasses[0].mountPod.cleanCache | string | `""` |  |
| storageClasses[0].mountPod.delayedMountDeletion | string | `""` |  |
| storageClasses[0].mountPod.image | string | `""` |  |
| storageClasses[0].mountPod.resources.limits.cpu | string | `"5000m"` |  |
| storageClasses[0].mountPod.resources.limits.memory | string | `"5Gi"` |  |
| storageClasses[0].mountPod.resources.requests.cpu | string | `"1000m"` |  |
| storageClasses[0].mountPod.resources.requests.memory | string | `"1Gi"` |  |
| storageClasses[0].name | string | `"juicefs-sc"` |  |
| storageClasses[0].pathPattern | string | `""` |  |
| storageClasses[0].reclaimPolicy | string | `"Delete"` |  |
| webhook.FailurePolicy | string | `"Fail"` |  |
| webhook.caBundlePEM | string | `""` |  |
| webhook.certManager.enabled | bool | `true` |  |
| webhook.crtPEM | string | `""` |  |
| webhook.keyPEM | string | `""` |  |
| webhook.timeoutSeconds | int | `5` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.3](https://github.com/norwoodj/helm-docs/releases/v1.11.3)
