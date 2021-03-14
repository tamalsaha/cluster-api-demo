# DigitalOcean

```
==> ubuntu-2004: Gracefully shutting down droplet...
==> ubuntu-2004: Creating snapshot: Cluster API Kubernetes v1.18.15 on Ubuntu 20.04
==> ubuntu-2004: Waiting for snapshot to complete...
==> ubuntu-2004: Destroying droplet...
==> ubuntu-2004: Deleting temporary ssh key...
Build 'ubuntu-2004' finished after 19 minutes 13 seconds.

==> Wait completed after 19 minutes 13 seconds

==> Builds finished. The artifacts of successful builds are:
--> ubuntu-2004: A snapshot was created: 'Cluster API Kubernetes v1.18.15 on Ubuntu 20.04' (ID: 80366900) in regions 'nyc1'
```

```
export DO_REGION=nyc1
export DO_SSH_KEY_FINGERPRINT=1991388
export DO_CONTROL_PLANE_MACHINE_TYPE=s-2vcpu-2gb
export DO_CONTROL_PLANE_MACHINE_IMAGE=80366900
export DO_NODE_MACHINE_TYPE=s-2vcpu-2gb
export DO_NODE_MACHINE_IMAGE=80366900
```

size-50-106


preflight: [preflight] Some fatal errors occurred:
[2021-03-14 18:40:51]   [ERROR KubeletVersion]: the kubelet version is higher than the control plane version. This is not a supported version skew and may lead to a malfunctional cluster. Kubelet version: "1.18.15" Control plane version: "1.17.11"

clusterctl config cluster capdo-quickstart \
    --infrastructure digitalocean \
    --kubernetes-version v1.18.15 \
    --control-plane-machine-count 1 \
    --worker-machine-count 3 > capdo-quickstart-cluster.yaml