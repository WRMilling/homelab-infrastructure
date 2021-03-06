# Mixed-architecture Kubernetes Cluster Setup Using k3s

## amd64

My x86_64 / amd64 nodes are built on top of Proxmox instead of bare metal nodes due to the hardware I have on hand. These will primarily be worker nodes in the cluster with one of the arm64 nodes acting as master. Please see the [amd64 README.md](amd64/README.md) for more information.

## arm64

My arm64 nodes consists of three 8GB Raspberry Pi 4 worker nodes. My long term goal is to have core services run on the low power arm nodes and in the event of a power failure, allow for longer overall runtime with my UPS by shutting down the higher power x86_64 nodes and running network + arm nodes for a longer period of time. Please see the [arm64 README.md](arm64/README.md) for more information.

## k3s setup

Once the cluster is built for the above architectures, check out [WRMilling/k3s-gitops Cluster Bootstrap](https://github.com/WRMilling/k3s-gitops/tree/master/setup) for bootstrapping the apps onto the infrastructure. 

## Credits

This section of `homelab-infrastructure` has an updated [LICENSE](LICENSE) to reflect the amount of work pulled from the [billimek/homelab-infrastructure](https://github.com/billimek/homelab-infrastructure/tree/master/k3s) - [License](https://github.com/billimek/homelab-infrastructure/blob/master/LICENSE).
