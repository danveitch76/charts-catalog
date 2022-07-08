# Default Helm-Values

Charts are primarily built to supply TrueNAS SCALE Apps.
However, we also supply Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume TrueCharts "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| hostNetwork | bool | `true` | Allow container access to host network |
| image.pullPolicy | string | `"IfNotPresent"` | When to pull image for container |
| image.repository | string | `"jc21/nginx-proxy-manager"` | Image to be used for container |
| image.tag | string | `"latest"` | Version of container image to pull |
| persistence.config.enabled | bool | `true` | Enable persistent storage of mountPath |
| persistence.config.mountPath | string | `"/data"` | Mount path for persistent storage |
| persistence.config.mountPath | string | `"/etc/letsencrypt"` | Mount path for persistent storage |
| persistence.varrun.enabled | bool | `true` | Image to be used for container |
| podSecurityContext.runAsGroup | int | `0` | The groupID this App of the user running the application |
| podSecurityContext.runAsUser | int | `0` | The userID this App of the user running the application |
| securityContext.readOnlyRootFilesystem | bool | `false` | Set root fole system to read only |
| securityContext.runAsNonRoot | bool | `false` | Set container to run as non-root |
| service.main.ports.main.port | int | `80` | The port exposed for access to this container on the service |
| service.main.ports.main.targetPort | int | `80` | The internal port on the container the Application runs on |
| service.main.ports.main.port | int | `81` | The port exposed for access to this container on the service |
| service.main.ports.main.targetPort | int | `81` | The internal port on the container the Application runs on |
| service.main.ports.main.port | int | `443` | The port exposed for access to this container on the service |
| service.main.ports.main.targetPort | int | `443` | The internal port on the container the Application runs on |

All Rights Reserved - Mr_Dan
