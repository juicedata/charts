# JuiceFS CSI Dashboard

配合 JuiceFS CSI Driver 使用，用于观测和排查。

```shell
# 部署的时候，注意命名空间需要对齐 CSI 驱动
helm upgrade -n kube-system --install juicefs-csi-dashboard .
```

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Juicedata Inc. | <team@juicedata.io> | <https://juicefs.com> |

## Source Code

* <https://github.com/juicedata/juicefs-csi-driver>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| envs | list | `[]` | Environment variables for the dashboard container Example:  - name: JFSCHAN    value: "gluster" |
| formatOptions | string | `""` | JuiceFS format options. Separated by spaces Example: "--inodes=1000000 --block-size=4M" Ref: https://juicefs.com/docs/community/command_reference#format |
| fullnameOverride | string | `""` |  |
| hostNetwork | bool | `false` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"juicedata/mount"` |  |
| image.tag | string | `"ce-v1.1.0"` | Overrides the image tag which defaults to the chart appVersion. For JuiceFS Community Edition, use ce-vx.x.x style tags For JuiceFS Enterprise Edition, use ee-vx.x.x style tags Find the latest built images in our docker image repo: https://hub.docker.com/r/juicedata/mount |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `"nginx"` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `""` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| port | int | `9000` |  |
| replicaCount | int | `1` |  |
| resources.limits.cpu | string | `"5000m"` |  |
| resources.limits.memory | string | `"5Gi"` |  |
| resources.requests.cpu | string | `"1000m"` |  |
| resources.requests.memory | string | `"1Gi"` |  |
| service.type | string | `"ClusterIP"` |  |
| tolerations | list | `[]` |  |
