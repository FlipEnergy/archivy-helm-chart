[![Artifact HUB](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/flipenergy)](https://artifacthub.io/packages/search?repo=flipenergy)

# This chart is no longer maintained.

# Helm chart for deploying Archivy to K8s
**Go to artifact hub for versions.**

Bare bones helm chart for deploying [Archivy](https://archivy.github.io/) to k8s. Support NFS as persistentVolume.

see [values.yaml](archivy/values.yaml) for configurations.

The app is configured to use elasticsearch by default but elasticsearch dependency is false. Create a PV and enable elasticsearch to use it.

Install using Helm v3:

```
helm repo add flipenergy https://flipenergy.github.io/k8s-homelab/
helm install my-release flipenergy/archivy
```

After the container is running, to create an admin account, exec in and run
```
archivy create-admin --password <your-password> <your-username>
```
